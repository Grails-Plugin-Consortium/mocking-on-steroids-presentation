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


!SLIDE shout
# Mocking Is Easy, Right?!


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
# Well... unless you want to mock your integration and functional tests


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
## Betamax, SoapUI, Third-party Solutions<BR /><br />These didn't meed our needs, were costly or all of the above.


!SLIDE quieter shout
# Service Virtualization<br /><span class="smaller">A <span class="danger">Smarter</span> Proxy</span>


!SLIDE quietest small-code 
# How about we also do these things

<ul>
    <li>Mock All Responses</li>
    <li>Enable Default Mock Responses</li>
    <li>Map Request Fields To Mocked Response Fields</li>
    <li>Enable Mockable State Transition</li>
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
