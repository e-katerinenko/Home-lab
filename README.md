# Detection and Response Lab
Inspired by <a href='https://blog.davidvarghese.net/categories/home-lab/'>David Varghese</a>
<img width="1700" height="1320" alt="Netwrok_GitHub" src="https://github.com/user-attachments/assets/68ca2992-0e25-4e44-92c9-55a1fb4bd1eb" />

<h1>🧪 Cybersecurity Homelab – Detection and Response</h1>

<h2>🎯 Objective</h2>
<p>
This homelab is designed to simulate real-world cyberattacks and incident response scenarios.
It enables hands-on practice with offensive and defensive security tools, digital forensics,
malware analysis, and centralized log collection and analysis.
The environment supports <strong>red team, blue team, and purple team workflows</strong>
in a controlled and safe manner.
</p>

<hr>

<h2>🏗️ Lab Overview</h2>
<p>
The lab is implemented using <strong>Oracle VirtualBox</strong> and is built around a
<strong>pfSense firewall</strong> that provides network segmentation, traffic control,
and security monitoring.
The pfSense VM is configured with <strong>six network interfaces</strong>:
one WAN interface and five isolated internal LANs, each serving a specific security function.
</p>

<hr>

<h2>🌐 Network Architecture</h2>

<h3>🔹 LAN0 – Management</h3>
<p><strong>Purpose:</strong> Administration and attack simulation<br>
<strong>VMs:</strong> Kali Linux</p>
<p>
Provides administrative access to the pfSense web interface and serves as the primary attack
platform for penetration testing, network enumeration, and Active Directory attack simulations.
</p>

<h3>🔹 LAN1 – Vulnerable</h3>
<p><strong>Purpose:</strong> Exploitation and post-exploitation practice<br>
<strong>VMs:</strong></p>
<ul>
  <li>Metasploitable2</li>
  <li>Chronos</li>
</ul>
<p>
Contains intentionally vulnerable machines used to practice vulnerability scanning,
exploitation, privilege escalation, and lateral movement techniques.
</p>

<h3>🔹 LAN2 – Active Directory</h3>
<p><strong>Purpose:</strong> Enterprise environment simulation<br>
<strong>VMs:</strong></p>
<ul>
  <li>Windows Server 2019 (Domain Controller)</li>
  <li>Windows 11 User VM 1</li>
  <li>Windows 11 User VM 2</li>
</ul>
<p>
Simulates a corporate Active Directory environment for practicing authentication attacks,
Kerberos abuse, credential attacks, lateral movement, and detection of suspicious domain activity.
</p>

<h3>🔹 LAN3 – Malware Analysis</h3>
<p><strong>Purpose:</strong> Safe malware analysis and reverse engineering<br>
<strong>VMs:</strong></p>
<ul>
  <li>FLARE-VM</li>
  <li>REMnux</li>
</ul>
<p>
An isolated network dedicated to static and dynamic malware analysis.
Direct connectivity to other internal networks is blocked.
File transfer is performed securely via <strong>SSH from the Tsurugi DFIR VM</strong>
to ensure containment and prevent accidental malware propagation.
</p>

<h3>🔹 LAN4 – Security</h3>
<p><strong>Purpose:</strong> Detection, investigation, and response<br>
<strong>VMs:</strong></p>
<ul>
  <li>Tsurugi Linux (DFIR and SOC platform)</li>
  <li>Ubuntu Linux with Splunk</li>
</ul>
<p>
Acts as the Security Operations Center (SOC) and Incident Response environment.
Centralized log analysis is performed using <strong>Splunk</strong>,
with a Splunk Forwarder configured on the Domain Controller.
Tsurugi is used for log analysis, network traffic inspection, timeline creation,
and forensic investigations.
</p>

<hr>

<h2>🔐 Skills</h2>
<ul>
  <li>Network segmentation and firewall rule enforcement using <strong>pfSense</strong></li>
  <li>Controlled attack simulation and lateral movement testing</li>
  <li>Active Directory attack and defense scenarios</li>
  <li>Malware analysis in a fully isolated environment</li>
  <li>Centralized log collection and correlation</li>
  <li>Digital forensics and incident response investigations</li>
  <li>Mapping attacker activity to <strong>MITRE ATT&amp;CK</strong> techniques</li>
</ul>

<hr>

<h2>🚀 Future Enhancements (Planned)</h2>
<ul>
  <li>Integration of IDS/IPS (Snort/Suricata) on pfSense</li>
  <li>Expanded detection engineering and custom alerting</li>
  <li>Additional attack scenarios and incident response playbooks</li>
  <li>Network traffic analysis and PCAP-based investigations</li>
</ul>
