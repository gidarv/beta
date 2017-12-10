# Infrastructure as Code in DevOps

If you’ve ever received a middle-of-the-night emergency support call because of a crashed server, you know the pain of searching through multiple spreadsheets, or even your memory, to access the manual steps of setting up a new machine from scratch. There is also an age-old difficulty: keeping the development and production environments consistent. An easier way to remove the possibility of human error when initializing machines and treat environments like code so that they are stood up from a single consistent definition is to use Infrastructure as Code.

A common analogy for using Infrastructure as Code is the distinction between owning pets and cattle. When you own pets, you give them names, you treat them individually, and if something bad happens to them, you care a lot. If you have a herd of cattle, you might still name them, but you treat them as a herd. In infrastructure terms, without treating environments as code, there might be severe implications if a machine crashes and you need to replace it (pets). If you use Infrastructure as Code, if a machine goes down, you can just spin up another machine with no issues (cattle).

### Configuration management

Before defining Infrastructure as Code, it is important to understand the definition of configuration management. Configuration management refers to the management of configuration of all environments for an application, typically in the form of version-controlled scripts. Managing the configuration of one application and environment can be challenging—imagine scaling this out manually for application across multiple servers.

Configuration management in DevOps is less formal than traditional configuration management. What this means is that encapsulation of configuration in code is favored over formal documentation, and that lighter-weight, executable configurations that allow having configuration and environments as code are valuable. Failed configuration can be very costly. As an example, consider the [Knight Capital fiasco](https://dougseven.com/2014/04/17/knightmare-a-devops-cautionary-tale/), in which the company suffered a $465 million trading loss and went bankrupt after releasing a new version of their high-speed algorithm software on five out of the six servers due to lack of automation. Had the company used automated, repeatable deployment, it might have avoided such a dramatic loss.

Infrastructure as Code and configuration as code both fall into the category of configuration management, and both relate to defining or scripting for environments. 

Infrastructure as Code is more specifically defined as follows:  Defining your environments to include networks, servers, and other compute resources as a text file (script or definition) that is checked into version control and used as the base source for creating or updating those environments. For instance, adding a new server is done by editing a text file and running the release pipeline, not by remoting into the environment and spinning up one manually.

When designing scripts or definitions for Infrastructure as Code, it’s important to make sure that the code and tools are set up to be *idempotent*, or able to run multiple times without error and with consistency. Infrastructure as Code can also be set up with developers' help, because many tools offer code that can be written in familiar programming languages—even ones as simple as JavaScript Object Notification (JSON) definitions.

Some examples of tools for working with Infrastructure as Code are: Vagrant, Ansible, Puppet, Chef, Docker, Windows PowerShell DSC, and cloud-provided tools such as Azure Resource Management templates.
