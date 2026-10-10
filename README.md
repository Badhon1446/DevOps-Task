# DevOps-Task

1: Explain what DevOps Engineering is. How does it differ from traditional development and operations roles?
DevOps Engineering is a way of working in which development (Dev) and operations (Ops) teams share responsibility for building, releasing and running software. A DevOps Engineer uses automation, CI/CD pipelines, monitoring and cloud tools to make releases fast, safe and repeatable.
In the traditional model, the two roles were separate:
Point	Traditional Dev and Ops	DevOps
Team structure	Developers and operations work in separate silos	One shared team and shared goals
Responsibility	Developers write code, then "throw it over the wall" to Ops	Everyone owns the product from code to production
Releases	Rare, large and risky	Frequent, small and automated
Problems	Blame passes between teams	Shared problem solving and learning
Testing and deployment	Mostly manual	Automated through pipelines
2: Describe how DevOps fits into the Software Development Life Cycle (SDLC). Mention at least three SDLC phases where DevOps adds value.
DevOps does not replace the SDLC. It runs through every phase of it and makes each phase faster and more reliable.
•	Planning: Developers and operations plan together, so infrastructure and deployment needs are known early. Example: using a shared issue tracker such as Jira or GitHub Issues.
•	Development: Version control (Git) and code review keep code organized. Example: every change goes through a pull request.
•	Build and Testing: a CI pipeline builds the code and runs automated tests on every push, so bugs are found early. Example: GitHub Actions runs unit tests automatically.
•	Deployment: CD pipelines release the code to servers without manual steps. Example: automatic deploy to staging, then production.
•	Operations and Monitoring: Tools such as Prometheus or Grafana watch the system, and the findings go back to the planning phase for the next improvement.
3: What values does a DevOps Engineer bring to an organization? Explain any four values with examples.
1.	Faster delivery: Automation shortens the time from writing code to users seeing it. Example: a feature that took two weeks to release now goes live in a day through a pipeline.
2.	Higher reliability: Testing, monitoring and rollback reduce outages. Example: a failed test blocks a bad release before it reaches users.
3.	Cost savings: Automation reduces manual work, and good cloud management avoids waste. Example: shutting down unused servers at night lowers the cloud bill.
4.	Better collaboration: Developers and operations share goals and tools, so there is less blame and more teamwork. Example: one shared incident channel where everyone solves a problem together.
4: Why is prior Software Engineering (SWE) experience considered helpful before becoming a DevOps Engineer?
A DevOps Engineer works closely with code, so knowing how software is built makes the job much easier.
•	Understanding the code: You can read an application's logs and errors and tell whether a problem is in the code or the infrastructure.
•	Scripting and automation: Pipelines and tools are written in languages like Python, Bash or YAML, which a software engineer already knows.
•	Version control and testing: Git, branching and testing are daily habits for developers and the core of CI/CD.
•	Empathy for developers: Knowing their daily problems helps you build tools they actually want to use.
•	Design knowledge: understanding architecture, databases and APIs helps you deploy and scale applications correctly.
A5: Explain why networking knowledge (DNS, ports, protocols, IP addressing) is important for DevOps roles.
Every application runs on a network, so many production problems are really network problems.
•	DNS: Turns a name like example.com into an IP address. If DNS is wrong, users cannot reach the site even though the server is running.
•	Ports: Each service listens on a port, for example HTTP on 80, HTTPS on 443 and SSH on 22. A closed or blocked port makes the service unreachable.
•	Protocols: HTTP, HTTPS, TCP and SSH define how systems talk to each other. Knowing them helps you debug failed connections and secure traffic.
•	IP addressing: Servers need correct public and private IPs, subnets and firewall rules to communicate safely.
Example: a website suddenly shows "cannot connect." With networking knowledge, you check DNS first, then whether port 443 is open, then the firewall rules, and find the cause quickly instead of guessing.
6: What soft skills are essential for a DevOps Engineer? Explain how these skills help during incidents or failures.
•	Communication: Short updates keep everyone informed. During an incident, "cause found, rollback in progress" stops confusion.
•	Collaboration and teamwork: DevOps connects many teams. Working together finds the cause faster than working alone.
•	Problem solving: Breaking a big failure into small checks leads to the root cause.
•	Staying calm under pressure: A calm engineer makes better decisions when the system is down.
•	Adaptability and willingness to learn: Tools change quickly, and every failure teaches something new.
•	Ownership and accountability: Taking responsibility for fixing the problem and writing a blameless post-mortem prevents repeat failures.
7: Explain the importance of patience and troubleshooting mindset in DevOps with a real-life example.
Most DevOps problems do not have an obvious cause. Patience lets you test one thing at a time instead of making random changes that create new problems. A troubleshooting mindset means asking: what changed, what is the evidence, and what is the smallest test I can run?
Real-life example: a doctor does not give random medicine. They ask about symptoms, run tests, rule out causes one by one, and only then treat the problem. DevOps works the same way.
DevOps example: after a deployment, users see "502 Bad Gateway." A patient engineer checks recent changes, then the application logs, then whether the service is running, and finally the proxy settings. The engineer finds that the app was listening on the wrong port. A hurried engineer who restarted every server would have wasted time and might have caused more damage.
Question 1: A new student joins a DevOps course but is unfamiliar with GitHub and cloud platforms. How would you onboard this student efficiently using tools, documentation, and communication channels?
A new student cannot learn everything at once, so I would onboard them in small steps: accounts first, then documentation, then hands-on practice, then support and follow-up.
Step 1: Set up accounts
•	Help the student create a GitHub account.
•	Help them open a free cloud account (AWS Free Tier or Render).
Step 2: Give simple documentation
•	Write a README.md that lists what to install (Git, VS Code, Python) and the order of the steps.
•	Share a short guide with screenshots, or a 5-minute video.
•	Provide a glossary that explains terms like repo, commit, branch and deploy in plain words.
Step 3: Hands-on practice
•	First task: create a repo, then commit and push one file.
•	Second task: deploy a small project to the cloud. Doing it themselves removes the fear.
Step 4: Communication channels
•	Add the student to a Slack, Discord or WhatsApp group.
•	Say clearly that asking questions is welcome.
•	Assign a mentor or buddy they can ask directly.
Step 5: Regular follow-up
•	Hold a short weekly check-in: where are they stuck, and what is unclear?
Question 2: During a production deployment, an application goes down unexpectedly. As a DevOps Engineer, describe step-by-step how you would troubleshoot and handle the situation.
Production is where real users use the application. Panicking makes mistakes worse, so I would work through the incident step by step.
1.	Stay calm and confirm the outage: Check whether the app is really down for everyone, or only for me (for example, my own internet).
2.	Tell the team: Post in the incident channel, "App is down, I am investigating." This stops people from duplicating work.
3.	Check recent changes: What changed in today's deployment? Most problems come from new code.
4.	Check logs and monitoring: Read the error messages and check server CPU, memory and disk.
5.	Fix fast with a rollback: If finding the cause takes time, go back to the last good version first. Restore service for users now; find the root cause later.
6.	Verify the fix: Confirm the app works again and keep watching monitoring for a while.
7.	Inform the team and stakeholders: Explain what happened and that the service is back.
8.	Write a post-mortem: Record the root cause and how to prevent it next time. The goal is learning, not blaming anyone.
Question 3: Your team releases features frequently, but system stability is decreasing. How can DevOps practices help balance speed and reliability?
Speed and reliability are not enemies. DevOps practices let a team have both.
•	CI/CD pipeline: Every code push is built and tested automatically. If a test fails, the change is not deployed.
•	Automated testing: Write tests in advance instead of relying only on manual checks.
•	Small releases: Ship one feature at a time rather than many together, so the cause of a problem is easy to find.
•	Staging environment: Try changes in a copy of production before real users see them.
•	Feature flags and canary releases: How a new feature to 5% of users first, then increase gradually if all is well.
•	Monitoring and alerts: Learn about problems before users report them.
•	Easy rollback: Return to the previous version in one click when something goes wrong.
•	Code review: Another person checks the code before it is merged.
Simple example: If you want a bus to go faster, it needs good brakes and seat belts. Safety is what lets you go fast.
Question 4: A team struggles with communication during incidents because members are distributed. How can proper onboarding to communication platforms improve DevOps workflows?
When team members work in different places, people do not know who is doing what during an incident, and confusion follows. Proper onboarding to communication tools greatly reduces this.
•	Everyone on the same platform: All members are already in Slack, Teams or Discord, so nobody searches for accounts during an emergency.
•	A dedicated incident channel: For example #incident, used only for urgent discussion so nothing gets lost.
•	Roles decided in advance: Who leads (Incident Commander), who investigates, and who sends updates.
•	Alerts delivered to the channel: Monitoring tools such as PagerDuty notify everyone at the same time.
•	A runbook: a written "what to do when the app is down" guide that even a new member can follow.
•	Regular practice: Run mock incidents (drills) so nobody panics during a real one.
•	Regular status updates: A short update every 15 minutes, such as "Cause found, rollback in progress."
•	Time zones in mind: The on-call roster clearly shows who is available and when.
Result: problems are found faster, work is not duplicated, and incidents are resolved sooner.



Task 1: Local DevOps Demo Application
Objective:
To run a simple web application on a local machine, verify that it is running successfully, and understand the importance of local application execution in DevOps workflows.Local application development is an important part of the Software Development Life Cycle (SDLC). Before deploying an application to a production server, developers run and test it in a local development environment. This helps them identify errors, verify application functionality, and ensure that the required dependencies are configured correctly.In DevOps, local development supports continuous integration and continuous delivery (CI/CD) by allowing developers to test code changes before they are integrated or deployed. It also helps reduce deployment failures and improves the overall software development process.
Procedure:
1.	Selected a web application for the local development environment.
2.	Configured the required environment and dependencies.
3.	Started the application on the local machine.
4.	Opened the application using the local URL in a web browser.
5.	Verified that the application was running successfully.
Result:
The application was executed successfully on the local machine and verified through a web browser.Running an application locally is an essential step in DevOps because it helps developers test, debug, and validate software before deployment. This improves software quality and reduces the risk of errors in the production environment.


<img width="1919" height="1006" alt="Screenshot 2026-10-10 140853" src="https://github.com/user-attachments/assets/37004923-3985-4fe4-8af8-b06fc656dea9" />
<img width="1919" height="882" alt="Screenshot 2026-10-10 141005" src="https://github.com/user-attachments/assets/2a84801b-f110-4e73-ac7f-e7bebc9009be" />
<img width="1919" height="951" alt="Screenshot 2026-10-10 141058" src="https://github.com/user-attachments/assets/398c3323-2b05-4777-b74a-d76fa1358cc3" />




Task 2: Exposing Local Application Using ngrok
To expose a locally running web application to the internet using ngrok, obtain a public URL, and understand the practical use of exposing local applications.Ngrok is a tunneling service that allows developers to make a locally running application accessible over the internet through a public URL. It creates a secure tunnel between a public endpoint and a service running on the local machine.In DevOps and software development, ngrok is useful for remote testing, client demonstrations, team collaboration, and testing webhook integrations. It allows developers to share an application with others without deploying it to a permanent public server.
Procedure:
1.	Started the web application on the local machine.
2.	Configured ngrok using an authentication token.
3.	Executed the command ngrok http 8000 to expose the local application running on port 8000.
4.	Copied the public HTTPS URL generated by ngrok.
5.	Opened the public URL in a web browser and verified that the application was accessible.
Real-World Use Case:
A developer can use ngrok to demonstrate a locally developed application to a client or team member before deploying it to a production server. It can also be used to test webhook integrations by allowing an external service to send requests to a local development application.
Result:
The local application was exposed to the internet through an ngrok public URL and verified using a web browser.Ngrok simplifies remote access to local applications and supports development, testing, and collaboration. It is a useful tool in DevOps workflows, particularly when an application needs to be tested or demonstrated before permanent deployment.
 
<img width="1919" height="1015" alt="Screenshot 2026-10-10 144659" src="https://github.com/user-attachments/assets/6be17e1e-fc7e-4cf7-8149-0cbee6556133" />

