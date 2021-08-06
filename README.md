# HashiCorp-Certified-Terraform-Associate
Reading list for Learning Terraform

## Setup Lab with Proxmox
Requirement for Terraform lab with Proxmox
* Proxmox host: a computer with installed Proxmox.
* Management host: management host for run command and build template with following tools
  * [Packer](https://learn.hashicorp.com/tutorials/packer/get-started-install-cli#installing-packer)
  * [Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli#install-terraform)
  * [Qemu/KVM](https://github.com/behradeslamifar/Linux-Professional-Institute-Certifications/tree/main/LPI304/labs#3303-kvm)
* Download `Ubuntu Cloud Image` from [Ubuntu website](https://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64.img)

### Version Table
Version of all tools that use in this repo
| Tools     |   Version   | 
| --------- |:-----------:|
| Ubuntu    | 20.04 Focal |
| Proxmox   | 6.4-1       |
| Packer    | v1.7.4      |
| Terraform | v1.0.3      |
| Qemu-kvm  | 4.2         |

## Objectives
1. Understand infrastructure as code (IaC) concepts
  * 1a Explain what IaC is
  * 1b Describe advantages of IaC patterns
2. Understand Terraform's purpose (vs other IaC)
  * 2a	Explain multi-cloud and provider-agnostic benefits
  * 2b	Explain the benefits of state
3. Understand Terraform basics
  * 3a	Handle Terraform and provider installation and versioning
  * 3b	Describe plugin based architecture
  * 3c	Demonstrate using multiple providers
  * 3d	Describe how Terraform finds and fetches providers
  * 3e	Explain when to use and not use provisioners and when to use local-exec or remote-exec
4. Use the Terraform CLI (outside of core workflow)
  * 4a	Given a scenario: choose when to use terraform fmt to format code
  * 4b	Given a scenario: choose when to use terraform taint to taint Terraform resources
  * 4c	Given a scenario: choose when to use terraform import to import existing infrastructure into your Terraform state
  * 4d	Given a scenario: choose when to use terraform workspace to create workspaces
  * 4e	Given a scenario: choose when to use terraform state to view Terraform state
  * 4f	Given a scenario: choose when to enable verbose logging and what the outcome/value is
5. Interact with Terraform modules
  * 5a	Contrast module source options
  * 5b	Interact with module inputs and outputs
  * 5c	Describe variable scope within modules/child modules
  * 5d	Discover modules from the public Terraform Module Registry
  * 5e	Defining module version
6. Navigate Terraform workflow
  * 6a	Describe Terraform workflow ( Write -> Plan -> Create )
  * 6b	Initialize a Terraform working directory (terraform init)
  * 6c	Validate a Terraform configuration (terraform validate)
  * 6d	Generate and review an execution plan for Terraform (terraform plan)
  * 6e	Execute changes to infrastructure with Terraform (terraform apply)
  * 6f	Destroy Terraform managed infrastructure (terraform destroy)
  * 7	Implement and maintain state
  * 7a	Describe default local backend
  * 7b	Outline state locking
  * 7c	Handle backend authentication methods
  * 7d	Describe remote state storage mechanisms and supported standard backends
  * 7e	Describe effect of Terraform refresh on state
  * 7f	Describe backend block in configuration and best practices for partial configurations
  * 7g	Understand secret management in state files
* 8	Read, generate, and modify configuration
  * 8a	Demonstrate use of variables and outputs
  * 8b	Describe secure secret injection best practice
  * 8c	Understand the use of collection and structural types
  * 8d	Create and differentiate resource and data configuration
  * 8e	Use resource addressing and resource parameters to connect resources together
  * 8f	Use Terraform built-in functions to write configuration
  * 8g	Configure resource using a dynamic block
  * 8h	Describe built-in dependency management (order of execution based)
* 9	Understand Terraform Cloud and Enterprise capabilities
  * 9a	Describe the benefits of Sentinel, registry, and workspaces
  * 9b	Differentiate OSS and TFE workspaces
  * 9c	Summarize features of Terraform Cloud

## Other Resources

### Hashicorp Documentation
* [Hashicorp: Terraform Associate Page](https://www.hashicorp.com/certification/terraform-associate)
* [Terraform Associate Review](https://learn.hashicorp.com/tutorials/terraform/associate-review)
* [Terraform Associate Certification - Study Guide](https://learn.hashicorp.com/tutorials/terraform/associate-study?in=terraform/certification)

### Recomanded Book
* [Terraform: Up and Running](https://www.terraformupandrunning.com/)
* [The Terraform Book](https://www.amazon.com/Terraform-Book-James-Turnbull-ebook/dp/B01MZYE7OY)

### Online Training
* [Cloud Guru](https://acloud.guru/overview/hashicorp-certified-terraform-associate-1?_ga=2.128822156.102402904.1627941239-2138038631.1606556224&_gac=1.53403354.1627744044.Cj0KCQjw6ZOIBhDdARIsAMf8YyFEA1vvDP570sIwxXWYCx94tdwohinimXEvnDCXQOqROkvWzgea4_saAul2EALw_wcB)

### Search
* [github](https://github.com/rfitzhugh/terraform-associate)
* [Blog post](https://nedinthecloud.com/2020/04/27/preparing-for-the-hashicorp-terraform-certification/)
