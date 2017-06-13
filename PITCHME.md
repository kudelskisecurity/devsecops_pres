### DevSecOps Lausanne meetup   
#### Fred Blaise, Kudelski Security
###### 13.06.2017
Shift Security left: make DevSecOps real

<span style="color:gray; font-size:0.4em">[Slides](https://gitpitch.com/kudelskisecurity/devsecops_pres/devsecops_meetup_062017) || [Source](https://github.com/kudelskisecurity/devsecops_pres/tree/devsecops_meetup_062017)</span>



<span style="color:gray; font-size:0.4em">Note: All stupid things I can say do not reflect my employer's view.
Great things may, however.</span>


---
<span style="color:gray; display:block; text-align:center">Before I forget...</span>

A couple events coming up
<span style="display:block; text-align:right; color:white">\+ [Soft-shake.ch](http://www.soft-shake.ch) (Oct. 26-27) - HEPIA, Geneva</span>
<span style="display:block; text-align:right; color:white">\+ [DevOps meetup](https://www.meetup.com/DevOps-Geneve/events/240232729/) (June 15) - Geneva</span>
<span style="display:block; text-align:right; color:white">\+ [KS Cyber Summit](https://www.kudelskisecurity.com/about-us/events/kudelski-security-cyber-summit) (June 15) - Lausanne</span>

And a plug
<span style="display:block; text-align:right; color:white">\+ I am hiring, infra engineer with security hat</span>

And a big thanks
<span style="display:block; text-align:right; color:white">\+ to our sponsor (look at the top-left logo)</span>
<span style="display:block; text-align:right; color:white">\+ My wife, who went shopping for our apero!</span>

---
<span style="color:gray; display:block; text-align:center">Embracing DevOps at KS engineering</span>

<!--- ![Masked Cucumber](assets/masked_cucumber_90px.jpg)  -->
![DevOps_SouthPark](assets/devops_southpark_400.png?style=centerimg)
<!--- ![ITIL is evil](assets/ITILisevil_avg.png?style=centerimg) -->

- Re-org + new management 
- Knock walls down (literally)
- Empower engineering leads
- Always-on "Designated ops" in "solutions" team
- Still in the early days of rolling out DevSecOps

Note:
- The re-org is important because it did rid part of a flawed organisation, which could not provide the needed level of performance to achieve our goals.
- Could get started with the right people, having the right mindset.
- Faster tech decisions

---
<span style="color:gray">Polymorphism</span>
* You've been telling your teams...
  * Build & run!
  * You own it, you're responsible for it!
  * You're on-call! 

<span style="display:block; text-align:right; color:white">\+ Now please, put your security hat on. <!-- .element: class="fragment" --></span>


<span style="display:block; color:rgb(0,148,147)">You need the right people. <!-- .element: class="fragment" --></span>


---
<span style="color:gray">A few challenges</span>

+++

<span style="color:gray">Where is your security design documented?</span>
<span style="display:block; text-align:right; color:white">... code over documentation! <!-- .element: class="fragment" --></span>


Note:
- Code over documentation
- Hence over security design documentation -- likely no documentation
- The fast iterations prohibits it

+++

<span style="color:gray">How much effort to put in security</span>
<span style="display:block; text-align:right; color:white">... to possibly just throw things away? <!-- .element: class="fragment" --></span>

+++

<span style="color:gray">Does everyone understand the complexity of</span>
<span style="display:block; text-align:right; color:white">... micro-services <!-- .element: class="fragment" --></span>
<span style="display:block; text-align:right; color:white">... containers <!-- .element: class="fragment" --></span>
<span style="display:block; text-align:right; color:white">... cloud <!-- .element: class="fragment" --></span>

Note:
* Vuln in containers
* or in underlying stacks used
* Secrets
* Bad security group in clouds
* floating IP on backend services
* No VPN?

+++

<span style="color:gray">How do you handle change</span>
<span style="display:block; text-align:right; color:white">... when you can deploy several times a day? <!-- .element: class="fragment" --></span>

Note:
Many small automated deployments Vs few big controlled ones
Remember the CAB once every 2 weeks to put a change through?

+++

<span style="color:gray">Separation of Duties</span>
<span style="display:block; text-align:right; color:white">What? Devs have access to prod? <!-- .element: class="fragment" --></span>
<span style="display:block; text-align:right; color:white">How do you demonstrate you still comply to auditors?<!-- .element: class="fragment" --></span>

Note:
Replace manual checks and gates with automated counterparts

---
<span style="color:gray">What is still present in a lot of places</span>
* Separation of duties (i.e., iso27001, cobit, itil), endless CABs
* Many (outside DevOps)
  * are still in favor of few big "controlled" changes
  * say do not touch unless it is broken
  * don't care much about technical debt
* Security still mainly at the perimeter
* InfoSec often lacks pure engineering skills 

Linus Torvalds says:  
> "Talk is cheap, show me the code."

I say:
> "Word&copy; docs are expensive, show me the code."

Note:
Classic org separates IT production from R&D
CorpSec is yet another split

---
<span style="color:gray">Where to get started</span>
<span style="display:block; text-align:right; color:white">Organizational change</span>

+++

<span style="color:gray">SecOps/CorpSec pros are usually no coders or infra guys</span>

<span style="display:block; text-align:right; color:white">\+ Security needs to be alive within the squad</span>
<span style="display:block; text-align:right; color:white">\+ Train your teams for security</span>
<span style="display:block; text-align:right; color:white">\+ Dedicate a champion</span>


<span style="display:block; color:rgb(0,148,147)">It is *hard* to find a pure DevSecOps guy.</span>

+++

<span style="color:gray">Make security a first class citizen</span>
<span style="display:block; text-align:right; color:white">\+ Publish your security status/metrics</span>
<span style="display:block; text-align:right; color:white">\+ Publish your changes</span>


<span style="display:block; color:rgb(0,148,147)">Establish trust and confidence.</span>

Note:
Security status, if possible, should be shown on a dashboard much like Jenkins job dashboard. If something fails, it needs to be tackled right away and fixed.

+++

<span style="color:gray">If you are a highly regulated company</span>
<span style="display:block; text-align:right; color:white">\+ Onboard your compliance team</span>
<span style="display:block; text-align:right; color:white">\+ Onboard your internal audit team</span>
<span style="display:block; text-align:right; color:white">\+ Onboard your management</span>

<span style="display:block; color:rgb(0,148,147)"> - Establish a true relationship </span>
<span style="display:block; color:rgb(0,148,147)"> - Work with them over the long haul to match their expectations</span>

+++

<span style="color:gray">Hush your ego, leverage talent around you</span>

![Sysadmin_day](assets/SysAdminDay.png?style=centerimg)
- Ask your Op or Dev friend for a hint

- Security reviews
  - Reviews are not only between Devs as "code reviews"
  - Can also happen between Ops, Devs and Secs guys


---
<span style="color:gray">Where to get started</span>
<span style="display:block; text-align:right; color:white">Infrastructure</span>

+++

<span style="color:gray">Frequent changes and updates are good for security</span>
<span style="display:block; text-align:right; color:white">\+ How long do you think it takes to prepare an attack?
<span style="display:block; text-align:right; color:white">\+ Most exploits are against legacy code
<span style="display:block; text-align:right; color:white">\+ Minimizes deployment risks over time

+++

<span style="color:gray">Logs management</span>
- Normalize your logs across all your components
- Enable real-time search across all your log sources
- Leverage dashboards
- Leverage automated alerts
- Enable log archives for compliance
- Leverage netflow

<span style="display:block; text-align:right; color:white">\+ [Graylog](https://www.graylog.org/)</span>

Note:
May not be very DevSecOps specifics, but it is super important

+++

<span style="color:gray">Infra as code</span>

We use a combination of [Puppet/Foreman/Katello](https://theforeman.org/) and [Jenkins](https://www.cloudbees.com/jenkins/jenkins-2)

<span style="display:block; text-align:right; color:white">\+ Automate your deployment </span>
<span style="display:block; text-align:right; color:white">\+ Merge request your infra </span>
<span style="display:block; text-align:right; color:white">\+ Consistency </span>
<span style="display:block; text-align:right; color:white">\+ Reduce config error/drift </span>
<span style="display:block; text-align:right; color:white">\+ Automatically install security updates </span>


Other products such as [UpGuard](https://www.upguard.com) or [CloudPassage](https://www.cloudpassage.com) can help too.

Note:
Example of ssh deployment issue with another puppet master

+++

<span style="color:gray">Harden everything</span>

- Harden your systems 
- Harden your configuration management ecosystem 
- Harden your CI/CD infrastructure and your code repositories
- Shutdown unnecessary services, reduce the attack surface
- Enable SElinux / apparmor
- Make sure logs are shipped to your central log management system

<span style="display:block; text-align:right; color:white">\+ [puppet-os-hardening](https://github.com/dev-sec/puppet-os-hardening)</span>
<span style="display:block; text-align:right; color:white">\+ [OSSEC](https://ossec.github.io)</span>

+++

<span style="color:gray">Know about your cloud basics</span>

Include in your pipeline as much as possible

<span style="display:block; text-align:right; color:white">\+ Scan security groups for ingress 0.0.0.0/0</span>
<span style="display:block; text-align:right; color:white">\+ Make sure your images are always up-to-date</span>
<span style="display:block; text-align:right; color:white">\+ Perform regular perimeter scans (never hurts)</span>

Note:
Cannot hurt to have regular scans if actually looking at results
Diff can be automated and possibly 

+++

<span style="color:gray">Introduce container scanning</span>

Containers you use most likely contain vulnerabilities.

<span style="display:block; text-align:right; color:white">\+ [Clair](https://github.com/coreos/clair "Clair") </span>
<span style="display:block; text-align:right; color:white">\+ [docker-bench-security](https://github.com/docker/docker-bench-security "docker-bench-security")</span>

Protect them with existing tech

<span style="display:block; text-align:right; color:white">\+ [Apparmor profiles](https://docs.docker.com/engine/security/apparmor/ "Apparmor profiles")</span>
<span style="display:block; text-align:right; color:white">\+ [Seccomp profiles](https://docs.docker.com/engine/security/seccomp/ "seccomp profiles")</span>

+++

<span style="color:gray">Secrets management</span>

Make sure your passwords, certificates or other keys are used in a safe manner.

<span style="display:block; text-align:right; color:white">\+ [Vault](https://www.vaultproject.io/ "Vault") from Hashicorp</span>
<span style="display:block; text-align:right; color:white">\+ [KeyWhiz](https://square.github.io/keywhiz/ "Keywhiz") from Square Engineering</span>

+++

<span style="color:gray">External assessment</span>

If at all possible, get a second -- outside -- opinion.

<span style="display:block; text-align:right; color:white">\+ [hackerone](https://www.hackerone.com) Vuln &amp; bug bounty platform</span>
<span style="display:block; text-align:right; color:white">\+ [Github security](https://bounty.github.com)</span>
<span style="display:block; text-align:right; color:white">\+ Red Vs Blue teams</span>
<span style="display:block; text-align:right; color:white">\+ Pen testing</span>
<span style="display:block; text-align:right; color:white">\+ Shared threat intelligence</span>


---
Questions? (and hopefully answers)


---
References
- Veracode: The Developer's Guide to the DevSecOps galaxy
- DevOps and Security: From the Trenches to Command Centers: https://blog.xebialabs.com/2017/05/04/devops-security-trenches-command-centers
- How Etsy makes Devops work: http://www.networkworld.com/article/2886672/software/how-etsy-makes-devops-work.html
- DevSecOps: http://www.oreilly.com/webops-perf/free/files/devopssec.pdf
- The treacherous 12: https://downloads.cloudsecurityalliance.org/assets/research/top-threats/Treacherous-12_Cloud-Computing_Top-Threats.pdf
- DevOps explained: https://www.niceideas.ch/roller2/badtrash/entry/devops-explained
- DevSecOps manifesto: http://www.devsecops.org
