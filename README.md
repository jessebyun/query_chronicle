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
<h3>Investigate the affected assets and events</h3>
