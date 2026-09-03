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
      Analyst should cheack more additional info like source ip locations ip 
