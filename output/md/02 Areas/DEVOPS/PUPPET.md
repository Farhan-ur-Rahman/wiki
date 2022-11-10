---
category: '2022'
created: 2022-11-09 20:49:29.479000+00:00
tags:
- areas
title: PUPPET
updated: 2022-11-09 20:54:05.678000+00:00
---
   
**What Is Puppet?**   
     
Puppet is a Configuration tool that is used for deploying, configuring and managing servers. To be more specific, puppet is responsible for   
   
   
-   Defining distinct configurations for each and every host, and continuously checking and confirming whether the required configuration is in place and is not altered on the host(if altered Puppet will revert back to the required configuration).   
-   Dynamic scaling-up and scaling-down of machines.   
-   Providing control over all your configured machines, so a centralised (master-server or repo-based) change gets propagated to all, automatically.   
-   Puppet uses a Master Slave architecture in which the Master and Slave communicate through a secure encrypted channel with the help of SSL.   
   
   
**Configuration Management**   
   
**System Administrators** usually perform repetitive tasks such as installing servers, configuring those servers, etc. They can automate this task, by writing scripts, but it is a very hectic job when you are working on a large infrastructure.   
   
To solve this problem, _Configuration Management_ was introduced. Configuration Management is the practice of handling changes systematically so that a system maintains its integrity over time. Configuration Management (CM) ensures that the current design and build state of the system is known, good & trusted; and doesn’t rely on the tacit knowledge of the development team. It allows access to an accurate historical record of system state for project management and audit purposes. Configuration Management overcame the following challenges:   
   
   
-   Figuring out which components to change when requirements change.   
-   Redoing an implementation because the requirements have changed since the last implementation.   
-   Reverting to a previous version of the component if you have replaced with a new but flawed version.   
-   Replacing the wrong component because you couldn’t accurately determine which component needed replacing.   
   
     
   
**How it works**    
   
   
-   Puppet has a configuration language, which is simpler than a traditional programming language. It is more like a markup language such as XML.   
-   A user uses this language to declare the items to be configured and the actions to be taken. This collection of instructions is saved as a ‘manifest’ file.   
-   While the user is doing this, they do not need to worry about the actual underlying platform. This is due to the resource abstraction feature of Puppet.   
-   To execute the configuration, Puppet picks the instructions while maintaining a graphical representation of the resources it has to act on (with their interdependencies). The configuration to be achieved (called the desired state) is achieved and the result of it is sent across to the server.   
   
**Advantages of puppet**   
   
     
Puppet is one the most popular configuration management tools around and has plenty of advantages.   
   
**Open source**   
   
     
It is important for a technology to be open source and hence be extendable. Puppet can be extended to build custom libraries and modules to suit the needs individual project.   
   
   
   
**Allows resource abstraction**   
   
   
It is possible for a configuration task today to be needed across a range of servers that all have different operating systems and other platform specific identities.   
   
Hoping that a system administrator actually remembers the commands and syntax of the individual platforms and reproducing that error-free is hoping for a lot.   
   
Puppet doesn’t need one to do that since it derives the system specific data using a utility called Factor. Factor helps Puppet know the system details like operating system, IP address etc. that helps Puppet achieve abstraction.   
   
   
**Puppet does a transaction only if needed**   
   
When the number of servers is as large as some systems have today, it is possible to encounter some form of redundancy. It is possible to have an instruction that doesn’t bring about any change in the system.   
   
Puppet has the feature of ‘idempotency’ which means it applies the changes asked for only when the changes would actually change something in the system. If the changes asked for are already done, Puppet doesn’t do anything. This is useful for achieving efficiency.   
   
   
   
**Boosts manageability and productivity**   
   
Puppet achieves significant improvements to the productivity of the system administrators. They are freed up from their mundane tasks and can actually concentrate on more advanced tasks that require human intervention. It also helps the server become more manageable with lesser effort and time.   
   
**Cross-platform**   
   
Puppet works on Fedora, RHEL, Debian, Gentoo, Solaris, OS X, and Windows. It helps the user to cover a wider range of platforms which makes more servers come into the configuration fold.   
   
   
**Puppet’s language is clean and easily learnable**   
   
Puppet’s declarative language is quite easy like writing an XML file. A person with limited programming knowledge can easily pick it up.   
   
   
**Puppet has crown-like support**   
   
Puppet can also help schedule specific maintenance actions on a periodic basis. This helps the administrators carry out some crown jobs in the maintenance cycle.   
   
**Override mechanism**   
   
The language supports a mechanism to override an instruction with a specific one for a different scenario. This is useful when exceptions are to be made while applying the configuration.   
   
**Puppet has an active community**   
   
Puppet being popular has an active community with plenty of active discussion boards, forums and experts willing to help out.   
   
     
   
**PDK VALIDATE** to check the code in vs code terminal   
   
     
   
**Puppet tasks** are written in the Puppet manifest language, and are used to automate the management of your Puppet infrastructure.   
   
     
   
 Tasks can be used to perform actions such as installing software, changing configuration settings, or applying patches.   
   
     
   
 Puppet tasks are made up of two parts: a resource type and a resource title. The resource type defines the type of resource that the task will manage, such as a file or a package.    
   
     
   
The resource title defines the name of the resource that the task will manage.    
   
     
   
**For example**, the following Puppet task would install the Apache web server:    
   
     
   
package { 'apache2': ensure => 'present' }    
   
     
   
This task would install the Apache web server package, and ensure that it is always present on the system.   
   
     
   
     
   
     
   
puppet is declarative   
   
consistent delivery   
   
increased productivity   
   
simplicity   
   
puppect is scaleable   
   
puppet is a pull based model   
   
     
   
IAC   
   
     
   
 INSTALLING PUPPET AGENT   
   
   
-   
   
yum install puppet-agent   
   
apt-get install puppet-agent   
   
install using EXE file   
   
     
**HIERA** is used to manage data in puppet.    
   
There are five levels of data priority: - default - environment - os - custom - global The priority is determined by the order in which the data sources are listed in the hiera.yaml file.   
   
     
   
 Data in the default data source takes the lowest priority. Data in the environment data source takes the next highest priority. Data in the os data source takes the next highest priority. Custom data sources can be defined in the hiera.yaml file.   
   
   
 These data sources take precedence over the default, environment, and os data sources.   
   
 The global data source always takes the highest priority. The data in this data source is used when no other data source contains a value for a given key.   
   
puppet uses the pull mechanism that is it is pulling the information from the nodes.