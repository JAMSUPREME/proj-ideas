# proj-ideas
Here's where I jot down ideas for things to build

# Infra
* Big bad orc - An orchestrator for build & deployment. The idea is that it would occasionally be nice to have something that sits on top of CI & Deployment (e.g. TeamCity or Bamboo & Octopus), especially since it is sometimes useful (when things are not continuously deployed) to group them together into a semantic release (e.g. R1 includes prod1 v3.0.0 and prod2 v1.2.1) - Advanced ideas might be mixing in tools (or allowing extensible connectors) for Hashicorp or AWS products, as well as CM stuff like Ansible/Puppet.
  * Feature toggle orchestration (an easy dashboard for toggling features for all environments) - This would necessitate some sort of syntax that big bad orc could read when deploying a release and then push changes to the client (maybe modifying a yml file)
  * Provisioning should be distinct from deployment - provisioning should be under the hood of the environment setup. It's also possible that each application has its own CloudFormation setup or scaling groups, etc. so that has to be considered.

# CSharp

* Nuget Nanny - I think this would somehow have to hook up with the CI or deployment system so that it is aware of all deployed products so it can manage the lifetime of all packages. Its purpose is to help clean up all the dead packages (e.g. -beta or even non-beta packages that just never got used). I imagine this is handy when lots of packages might be popped out every time a commit happens if the pkg generation is part of the CI setup

# Ruby

* Questionnaire - Some sort of helper lib for setting up a question-based workflow. e.g. Q1 might branch to Q2 OR Q3, Q2 AND Q3, or Q4, etc...

# Rust

* "Tin-plates" templates. Use basic lang syntax to do templates? e.g. `html()`, `div()`, etc.
