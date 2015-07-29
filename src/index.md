# Grails Mocking On Steroids

by <a href="https://twitter.com/ctoestreich">@ctoestreich</a>


!SLIDE shout
# Grails <span class="danger">Mocking</span><br />On Steroids

## by <a href="https://twitter.com/ctoestreich">@ctoestreich</a>


!SLIDE quiet small-code 

# Christian Oestreich

## <b>OSS org:</b> Grails Plugin Consortium
## <b>Github:</b> https://github.com/Grails-Plugin-Consortium

<br />
<img src="images/logo.gif" alt="bluestem group">
## <b>Company:</b> Bluestem Group
## <b>Url:</b> http://www.bluestembrands.com/

!SLIDE quiet small-code 

# Back In The Day
## Everything was manual

<img src="images/devops-define-roles.jpg" alt="dev ops">

!SLIDE quiet small-code 

# In The Now
## Everything is automated

<img src="images/docker.jpg" alt="dev ops">


!SLIDE quiet small-code 

# In The Now

<img src="images/deploy.png" alt="automated deploy" height="80%">


!SLIDE shout 
# We run <span class="danger">a lot</span> tests


!SLIDE quiet small-code 
# Running <span class="danger">a lot</span> of the same functional tests on transactional systems cause corrupted test data


```
    given:
    assert customer.payments.size() == 0
    
    when:
    customer.makePayment()
    
    then:
    customer.payments.size() == 1
   
```

!SLIDE shout
# Mocking Is <span class="danger">Easy</span>, Right?!


!SLIDE quiet small-code 
# Well Of Course!

## Spock, Mockito, etc.


```
   //Spock
   ServiceClass serviceClass = Mock(ServiceClass)
   
   //Mockito
   List mockedList = mock(List.class);
   
   //EasyMock
   List testDouble = EasyMock.createMock(List.class);
   
   //PowerMock
   MyClass myClassMock = PowerMock.createMock(MyClass.class); 
   
```


!SLIDE quietest shout 
# Well... unless you want to mock your external systems during integration and functional tests


!SLIDE shout

<img src="images/whoa.jpg" alt="whoa" width="75%">


!SLIDE quietest shout 
# "The systems behind your system don't always need to be exercised to prove your system is operating and ready for continuous deployment" -me
## #microservices #boundedcontext


!SLIDE quietest small-code 
# In our SOA we needed a way to accomplish the following

<ul>
    <li>Have Reliable Success Conditions</li>
    <li>Have Reliable Fail Conditions</li>
    <li>Avoid Backend System Outages</li>
    <li>Support Continuous Deployment via Functional Tests</li>
    <li>Int & Funct Tests Pass or Fail Fast</li>
</ul>


!SLIDE quieter shout
# Tools we looked at
## Parasoft, Betamax, SoapUI, Third-party Solutions<BR /><br />These didn't meet our needs, not pci compliant,<br />were costly or all of the above.


!SLIDE quieter shout
# Service Virtualization<br /><span class="smaller">A <span class="danger">Smart</span> Proxy</span>

!SLIDE quiet small-code 
# Service Virtualization
<img src="images/stack.png" alt="stack" height="60%">


!SLIDE quiet small-code 
# Service Virtualization
<img src="images/tracer.jpg" alt="tracer" height="70%">

!SLIDE quietest small-code 
# How about we also do these things

<ul>
    <li>Mock Responses <i>(matched input)</i></li>
    <li>Enable Default Mock Responses <i>(unmatched input)</i></li>
    <li>Map Request Fields To Mocked Response Fields <i>(echo)</i></li>
    <li>Enable Mockable State Transition <i>(#winning)</i></li>
    <li>Enable Transparent Proxy</li>
    <ul>
    <li>Record Live Data</li>
    <li>Replay Recorded Data</li>
    <li>Cache Responses</li>
    <li>Cache Pre-Fetching</li>
    <li>Monitor Service Calls (Hystrix)</li>
    </ul>
</ul>

!SLIDE shout

<img src="images/allthings.jpg" alt="whoa" width="75%">

!SLIDE quietest small-code 
# Why Grails?

<ul>
   <li>CXF Plugin</li>
   <li>CXF Client Plugin</li>
   <li>Redis Plugin</li>
   <li>Jesque Plugin (async jobs)</li>
   <li>Hystrix Plugin</li>
   <li>Restful Controllers</li>
   <li>CRUD Dashboard Easy</li>
</ul>

!SLIDE quietest small-code 
# Source Code

<ul>
<li>Backend Server<br /><a href="https://github.com/Grails-Plugin-Consortium/gr8conf-services">https://github.com/Grails-Plugin-Consortium/gr8conf-services</a></li>
<li>Smart API (Cache, Mock, Monitor)<br /><a href="https://github.com/Grails-Plugin-Consortium/gr8conf-smart-api">https://github.com/Grails-Plugin-Consortium/gr8conf-smart-api</a></li>
</ul>
 

!SLIDE small-code push-content-down
# Demo Time 

Lets Demo This


!SLIDE shout
# Questions? 
