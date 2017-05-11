<h1>Overview</h1>
<p><a href="http://hapihq.com">The HAPI Project</a></p>

<ul>
  <li><a href="#systemoverview">System Overview Image</a></li>
  <li><a href="#smart">Smart Module</a></li>
    <li><ul><li><a href="#smart-req">System Requirements<a></li></ul></li>
  <li><a href="#dumb">Dumb Module</a></li>
    <li><ul><li><a href="#dumb-req">System Requirements<a></li></ul></li>
</ul>  

![System Overview](/../../readme/system-overview.png)
<p>Please be advised: This image is representing a previous design of the project. We're currently redesigning it and we'll update the image as soon as possible.</p>
<a name="systemoverview" />  
  <h2>System Overview</h2>
  <p>Explain briefly how the system will work.</p>
  <p>If possible add some image as an example.</p>

<a name="smart" />
  <h2>Smart Module (former RTU/ST)</h2>
  <p>Smart Modules are devices with a high computational capability that can perform large operations, such as: Raspberry Pi 3 and Raspberry Pi Zero.</p>
  <p>We call Smart Module not simply because they have more CPU power, but they can exchange functionalities, work with TLS/SSL to improve security and much more.</p>
  <p>The main idea behind a Smart Module is to support a redundancy system. As explained above on <a href="#systemoverview">System Overview</a> the MQTT Broker (Server) is responsible to store all the data being transmitted. If for some reason this Server is unreachable (configuration problems or hardware failure, for instance), any other Smart Module within the system can step up and take its place.</p>
  <p>Note: Smart Module will work on top a modified version o Raspbian.</p>
  <a name="smart-req" />
  <h3>System Requirements</h3>
    <p>Smart Module run on top of a slightly modified Raspbian image (<a target="_blank" href="https://www.raspbian.org/">https://www.raspbian.org/</a>)</p>
    <p>The necessary packages are:</p>
    <ul>
      <li><b>Mosquitto</b></li>
      <li><b>Avahi</b></li>
      <li><b>SQLite3</b></li>
      <li><b>Python Packages</b>:
        <ul>
        <li><b>Paho MQTT</b>: The Eclipse Paho project provides open-source client implementations of MQTT and MQTT-SN messaging protocols aimed at new, existing, and emerging applications for the Internet of Things (IoT).</li>
        <li><b>Schedule</b>: Schedule lets you run Python functions (or any other callable) periodically at pre-determined intervals using a simple, human-friendly syntax.</li>
        <li><b>Serial</b>: This module encapsulates the access for the serial port.</li>
        <li><b>Twilio</b>: The twilio-python helper library lets you write Python code to make HTTP requests to the Twilio API.</li>
        <li><b>InfluxDB</b>: InfluxDB-Python is a client for interacting with InfluxDB.</li>
        <li><b>psutils</b>: psutil is a cross-platform library for retrieving information onrunning processes and system utilization (CPU, memory, disks, network)in Python.</li>
        </ul>
      </li>
    </ul>

<a name="dumb" />
  <p>[MARKED TO BE REVIEWED]</p>
  <h2>Dumb Module (former RTU)</h2>
  <p>Dumb Modules aren't really dumb. Indeed they're quite good to run everything we need to an actual working and functional Remote Terminal Unit. Although they have less capabilities if compared with Smart Modules. Until now we're currently working with Arduino Mega 2560.</p>
  <p>We're making plans to include NodeMCU support as well.</p>
  <a name="dumb-req" />
  <h3>System Requirements</h3>
    <p>Will be updated soon</p>
