<h1>Analyze a Phishing Incident</h1>

Scenario - Received an alert that an employee received a phishing email in their inbox. Upon review, identified a suspicious domain name contained in the email's body:  "signin.office365x24.com". To investigate further I will utilize Chronicle to determine whether any other employees have received phishing emails containing this domain and whether they have visited the domain. 
<br/>
<br/>

<h2>Domain search</h2>
<img src="https://i.imgur.com/2KSovJy.png" alt="1"/>
Observed when typing in domain name "signin.office365x24.com" in the search bar it is listed, indicating that domain exists in the ingested data. 
<br/><br/><br/>

<h2>Evaluate the search results</h2>
<img src="https://i.imgur.com/f4oUCS6.png" alt="2"/>
Prevalence section provides a graph which outlines the historical prevalence of the domain. Can see that the domain was accessed by six distinct assets or employees. Domains with less prevalence can indicate a great threat. RESOLVED IPS insight card indicates that there are two IP addresses that map to signin.office365x24.com. SIBLING DOMAINS insight card indicates login.office365x24.com as a sibling domain, which shares the same top domain office365x24.com with the domain I am investigating: signin.office365x24.com. 
<br/><br/><br/>

<h2>Investigate the threat intelligence data</h2>
<img src="https://i.imgur.com/qTRpm2R.png" alt="3"/>
To investigate the Top Private Domain, clicked on link to access the domain view for office365x24.com. Accessed VT CONTEXT to access the VirusTotal information about this domain. In the pop up, observed that 5 security vendors has flagged this domain as malicious. Also under WHOIS LOOKUP can observe the registration information for the domain owner such as name and contact information. This can help assess the domain's reputation and determining the origin of malicious websites. 
<br/>

<p>
  <img src="https://i.imgur.com/Gauh0ww.png" align=right>
  <br/><br/><br/>
  <p align=center></p>ET INTELLIGENCE REP LIST insight card also reveals threat intelligence information about this domain category being: Drop site for logs or stolen credentials</p>
</p>
<br/><br/><br/><br/><br/>

<h2>Investigate the affected assets and events</h2>
Information about the events and assets relating to the domain are separated into the two tabs: TIMELINE and ASSETS. 

<table>
<tr>
<td width="65%">
  <!-- Image goes here -->
  <img src="https://i.imgur.com/6KqAxqS.png" alt="image"/>
</td>
<td>
  <!-- Text goes here -->
  To investigate affected assets and events, went back to the domain view for the original domain search: signin.office365x24.com. By clicking on timeline I can see there are 24 events. Each event with a timestamp, asset identifier, and name of domain. 
</td>
</tr>
</table> 
<br/><br/><br/>

<img src="https://i.imgur.com/0rt34yr.png" alt="image"/>
Clicking on EXPAND ALL, details can be revealed about the HTTP requests made, including GET and POST requests. POST information is especially useful because it means that data was sent to the domain. It also suggests a possible successful phish. By clicking on an event, further information is provided from the raw data log of each specific event. 
<br/><br/><br/>

<img src="https://i.imgur.com/VSZSvT7.png" alt="image"/>
Clicking on the ASSSET tab, there are 6 assets that interacted with this domain. When clicking on a date on which the asset made interaction with the domain, there is further information that is populated. Information such as IP address, MAC address, dates when there was interaction with timestamps. 
<br/><br/><br/>

<h2>Investigate resolved IP address</h2>
<img src="https://i.imgur.com/BQqIBG0.png" alt="image"/>
Information was collected about the domain's reputation using threat intelligence, and I've identified the assets and events associated with the domain. Based on this information, it's clear that this domain is suspicious and most likely malicious. There is also one last thing to investigate. Attackers sometimes reuse infrastructure for multiple attacks. In these cases, multiple domain names resolve to the same IP address. Under the RESOLVED IPS insight card, I can investigate the associated IP address to identify if multiple domains use the same IP. 
<br/><br/><br/>


