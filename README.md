config-mgmt-utilities
=====================

A list of utilities to support configuration management tools.

This was produced by the panelists of the Configuration Mgmt Workflow panel at LOPSA-EAST in 2013.

One of the attendees also took notes:  http://verticalsysadmin.com/blog/uncategorized/highlights-from-lopsa-east-2013-configuration-management-workflows-panel


-------



Individual level: IDE / syntax highlighting etc  
Puppet: vim - https://github.com/rodjek/vim-puppet  
 TextMate & sublime text 2 - https://github.com/masterzen/puppet-textmate-bundle  
 gepetto (http://cloudsmith.github.io/geppetto/), emacs  

Chef: vim, TextMate, sublime text 2, emacs?  
  Sublime Text: http://www.youtube.com/watch?v=4VtDj_ar1Xg (video), https://github.com/cabeca/SublimeChef (GitHub)  
  Emacs: chef-mode https://github.com/mpasternacki/chef-mode  

CFEngine:
  vim - https://github.com/neilhwatson/vim_cf3
  emacs - https://github.com/cfengine/core/blob/master/contrib/cfengine.el
  kate - https://github.com/cfengine/core/blob/master/contrib/katepart-cfengine.highlight.xml
  eclipse - https://cfengine.com/eclipse-cfengine-editor
  Sublime Text - https://github.com/kebori/sublime-cfengine3

Local Testing  
Vagrant -   
VMware  
OpenStack  
Cloud?    
All of the above?

Revision Control : Which tool? Which workflow?   
Github Flow - http://scottchacon.com/2011/08/31/github-flow.html  
git-flow - http://nvie.com/posts/a-successful-git-branching-model/  
Git Dynamic Environments - https://puppetlabs.com/blog/git-workflow-and-puppet-environments/  , https://github.com/adrienthebo/puppet-git-hooks

Commit hooks  
Puppet: erb, pp parser, yaml, https://github.com/puppetlabs/puppetlabs-training-bootstrap/blob/master/modules/fundamentals/files/pre-commit  
Chef: fc pre-commit: https://github.com/gregf/chef-git-hooks  
CFEngine:
  Subversion: http://worrbase.com/2012/07/11/cfengine-svn-pre-commit.html
  Git: https://github.com/cfengine/design-center/tree/master/tools/git-pre-commit

Style / Lint tools  
Puppet: puppet-lint - http://puppet-lint.com/, https://github.com/santana/puppet-cleaner,   
Chef: tailor, foodcritic  
CFEngine: cf-promises (with GCC-style warnings)

Testing manifests / recipes   
Puppet: rspec-puppet, ?cucumber-puppet (discontiued)?  
Chef: chefspec, minitest-handler, rspec-chef, cucumber-chef, test-kitchen  

Marshalling / Assembling Code & Dependencies  
Puppet: librarian-puppet - https://github.com/rodjek/librarian-puppet  
Chef: berkshelf, librarian  
CFEngine: cf-sketch - https://github.com/cfengine/design-center/wiki/Design-Center-Tools

Continuous Integration  
Jenkins CI  
Travis CI   
Atlassian Bamboo?  
TeamCity?  

Orchestration  
Puppet: MCollective  
Chef has “knife ssh” and Pushy support coming for push jobs  

Canary testing  & Prod vs QA  vs test environments (not prod vs QA app code)  
serverspec http://serverspec.org/  
rspec-system https://github.com/puppetlabs/rspec-system  
nagios checks/ plugins  

Chef has knife-flip from Etsy, flips nodes into a test environment  

CFEngine: Remote context class matching using remoteclassesmatching (Enterprise)

Provisioning VM's in the cloud?  
Chef:  
knife ec2 server create...  
spiceweasel somefile.yml  
knife openstack...  
knife <cloudprovider> server create...  
  
Clouds include Azure, Openstack, Rackspace, etc.  

EC2 OpsWorks (although some limitations since it’s an older version)  

Puppet:  
puppet node_aws create / puppet node_vmware create  
Puppet RAL for AWS, OpenStack, CloudStack:  
    ec2_instance { “instance_name”:
      type => t1.large,
      az   => ‘USWest’,
      ensure => present,
      ….
    } 
Razor (bare metal)  

CFEngine: https://github.com/cfengine/design-center/tree/master/sketches/cloud

Crowbar has Chef server integrated, although I don’t know that much about it.  
Joyent also has a Chef “dataset” that they support.  
  
Team Workflow  
Puppet: -?  
Chef: knife-spork (has handlers to notify people)  
