YOUR TASK

SCENARIO 1

A user successfully logs in to their company account during normal working hours.
1. Is this an event, alert, or incident?

ans: event

 2. Why?

ans: a login from user on company account happened during office hours so its a normal login so it has recorded as an event

SCENARIO 2

A security system detects 15 failed login attempts for the same user account within two minutes.

1. Is this an event, alert, or incident?

ans: alert

2. What information should an L1 analyst check?
   
ans: what was username involved?
     what was date and time?
     which system was used?
     what was source ip address?
     weather there was successful login after 15 failed login?
     what was the location from attack happen?


  3. Would you immediately call this a confirmed attack? Why?
  
  ans: no we cannot call this an attack we need to investigate more and if necessary we need to escalate this


SCENARIO 3

An analyst investigates suspicious login activity and confirms that an unauthorized person accessed the employee's
account.

1. Is this an event, alert, or incident?

ans: incident

2. Why?

ans:when a analyst confirm that account has been hacked after deep investigation then it is an incident 



SHORT SCENARIO — BASIC ALERT TRIAGE

Alert:
User: Rahul
Source IP: 203.0.113.50
Failed Login Attempts: 15
Time: 2 minutes

Answer the following:

1. What happened?

ans: Rahul's account had 15 failed login attempts within 2 minutes from the same source IP. This is suspicious login activity and generated an alert.

2. What information would you check first?

ans: source IP address and its location
      15 attempts came from the same IP
      Whether there was a successful login after the failed attempts
      date and time 
      system logs 


3. Is there enough information to confirm an incident?

ans: no we need to investigate more to confirm it is incident or not 


4. What should the L1 analyst do next?

ans: SOC analyst L1 will investigate the alert more deeply by additional information and if needed then escalate will that 
