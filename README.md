# Open-redirect-stored-leads-to-XSS

	Open redirect(stored) leads to XSS					
	Summary:					
	Stored open redirect link with xss payload in profile, and anyone who will check that profile and click on the link the XSS will trigger.					
	Description:					
	Open redirection vulnerabilities arise when an application incorporates user-controllable data into the target of a redirection in an unsafe way .Stored open redirection vulnerabilities arise when the applicable input was submitted in an previous request					
	 and stored by the application. This is often more serious than reflected open redirection because an attacker might be able to place persistent input into the application which, when viewed by other users, causes their browser to trigger xss.					
	Steps to Reproduce:					
1.	Go to https://hushl.in					
2.	Create two accounts - Account1=attacker & Account2=user					
3.	Under Account1, go to Profile and click on Edit Profile					
4.	Enter this payload javascript://https://whitelisted.com/?z=%0Aalert(1) under Your Website Link and click Save.					
5.	Now, login into Account2 and search for Account1 with its username and open profile					
6.	After opening the Account1 profile in Links: section click on the Website link given(web logo)					
7.	You will see the redirection and then XSS will trigger.					
	Demonstration of Vulnerability:					
	POC1: https://clipchamp.com/watch/YwwwJjsCUII     (Account1)
					
	POC2: https://clipchamp.com/watch/5eRYSz2zZlh          (Account2)
					
	POC3: https://clipchamp.com/watch/gU4eVf5MYvP    (All in one)					

Impact:					
Attacker can make user redirect to malicious website and aslo attacker can still cookies who clicks on the link					
