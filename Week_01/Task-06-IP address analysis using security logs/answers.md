PART 1 — IP ADDRESS ANALYSIS

answers the following questions

1. List all unique source IP addresses found in the log.

The unique source IP addresses are:

192.168.1.25

192.168.1.30

10.0.0.15

198.51.100.24

203.0.113.50

192.168.1.42

10.0.0.32

198.51.100.77

10.0.0.12

10.0.0.30


2. Identify which source IP addresses belong to private IP ranges.?

ans:

The private source IPs are:

192.168.1.25

192.168.1.30

10.0.0.15

192.168.1.42

10.0.0.32

10.0.0.12

10.0.0.20



3. Identify which source IP addresses are external/public based on the log data.

ans:

Based on the log data, the external/public source IPs are:

198.51.100.24

203.0.113.50

198.51.100.77


4. List all destination IP addresses that belong to private IP ranges.

The private destination IPs are:

ans:

10.0.0.10

10.0.0.25

10.0.0.5

10.0.0.20

10.0.0.40


5. Identify two examples of communication between internal systems.

ans:

Example 1:
192.168.1.25 → 10.0.0.10
Rahul successfully logged in to the web server.

Example 2:
10.0.0.32 → 10.0.0.40
Vikram accessed files on the file server.


6. Identify two examples where an internal system communicates with an external address.

ans:

Example 1:

192.168.1.30 → 8.8.8.8

Example 2:

192.168.1.42 → 93.184.216.34



PART 2 — PATTERN IDENTIFICATION

1. Which source IP address appears repeatedly during failed login attempts against the database server?

Ans: 203.0.113.50

2. How many failed login attempts are shown for that activity?

Ans: 5 failed login attempts

3. Which username is being targeted during those attempts?

Ans: admin

4. Identify another source IP associated with repeated failed login attempts.

Ans: 198.51.100.77

5. Which destination systems are involved in the repeated failed login activity?

ans: 10.0.0.20 → Database server (db01)
     10.0.0.10 → Web server (web01)

6. Do repeated failed logins automatically prove that an account was compromised? Explain briefly.

Ans: No,Repeated failed logins indicate suspicious activity, but they do not prove that the account was compromised.
      Analyst should check more additional info like source ip locations destination ip location involved system names and users 

PART 3 — TRICKY INVESTIGATION SCENARIOS

1. VPN login for Amit: successful → failed → successful from same IP. Does this automatically indicate an attack?

Ans: No, it does not automatically indicate an attack.

2. Admin has failed logins from external IP, then successfully logs in from a different private IP. Can we conclude external access?

Ans: No, we cannot conclude that the external source successfully accessed the account.

The failed attempts came from:

203.0.113.50 → 10.0.0.20
Username: admin
5 failed attempts

Later, the successful admin login came from:

10.0.0.12 → 10.0.0.20

These are different source IP addresses. The log does not show a successful login from 203.0.113.50.

3. DNS queries to public IP addresses — automatically suspicious?

Ans: No.

Communication with a public/external IP address does not automatically mean malicious activity.

4. User successfully accesses a file server from a private IP. What additional information is needed?

ans: We would need to check:

Which user accessed the file

Which files/folders were accessed

Whether the user was authorized to access them

What action was performed — read, copied, modified, deleted, etc.

Whether the activity happened during normal working hours

Whether the user's device/IP is normally associated with that user

Whether there were any unusual downloads or large file transfers

5. Which event should be prioritized for investigation first?

Ans: The repeated failed admin logins against the database server from 203.0.113.50.

PART 4 — INVESTIGATION QUESTIONS

1. Identify two activities that appear normal based on the available context.

ans: Rahul's successful SSH login

     Vikram's file access

2. Identify two activities that require further investigation.

ans:  Repeated failed admin logins from 203.0.113.50 to the database server.

      Repeated failed root logins from 198.51.100.77 to the web server.

3. What makes each activity interesting or unusual?

ans: Admin login failures

     Root login failures

4. What additional information would you check before confirming malicious activity?

ans: Source IP reputation and location

     User's normal login behavior
  
     Device information

     Login time and frequency

     Whether a successful login happened after the failures

 5. Why is context more important than looking at an IP address alone?

ans: Because an IP address by itself does not tell us whether an activity is normal or malicious.    




PART 5 — SHORT ANSWERS

1. What does a source IP represent?

ans: dource ip represent from where it came from

2. What does a destination IP represent?

ans:  it represent that where is the destination address where to get delivered 

3. Is 192.168.1.25 a public or private IP address?

ans: private ip address

4. Is 10.0.0.15 a public or private IP address?

ans: public ip address

5. Which field in a log helps identify when an event occurred?

ans: date and time 

6. Which field identifies whether an authentication attempt succeeded or failed?

ans: status 

7. Can an IP address alone confirm that an attack occurred?

ans: no

8. What is one reason repeated failed logins may require investigation?

ans: 
