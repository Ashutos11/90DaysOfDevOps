### What is infrastructure as Code(IaC)? Why does it matter in DevOps?

Infrastructure as Code(IaC) is managing and provisioning infrastructure(Servers, networks and databases) through a machine-readable definition files rather than manual physical configuration.

It helps Devops teams to automate provisioning, ensure consistent environments and scale rapidly.

### What problem does IaC solve compared to manually creating resources in the AWS console?

It solves the problem of slow provisioning of servers by IT and inconsistent infrastructure.

### How is Terraform different from AWS CloudFormation, Ansible and Pulumi?

Terraform is owned by Hashicorp and releases frequent updates which makes it users to use and provision infrastructure. Whereas AWS CloudFormation can only be used in AWS, Ansible is a configuration management tool and Pulumi uses general programming languages like Python, C#, Java, TypeScript to provision infrastructure. Terraform uses HashiCorp Configuration Language(HCL) Language to define infrastruture.

### What does it mean that Terraform is "declarative" and "cloud-agnostic" ?

Declarative means we just have to define the desired state and Terraform will perform actions to achieve that state. Cloud-agnostic means Terraform uses same language to provision different cloud resources.

### What did `terraform init` download? What does the `.terraform/` directory contain?

It downloaded a specific hashicorp aws provider version along with few plugins. The directory contains a series of folders inside which terraform aws provider exe is kept along with its license file.

### How does Terraform know the S3 bucket already exists and only the EC2 instance needs to be created?

Terraform tracks created resources using a state file which acts as a single source of truth about the infrastructure is manages.

### What information does the state file store about each resource?

It stores unique id of the resource, properties, metadata and dependency information.

### Why should you never manually edit the state file?

Because Terraform depends on this file to manage infrastructure, if any thing happens infrastructure changes are irreversible.

### Why you should never commit state files into git?

- They pose security risks as they store many information in plain text.
- State files are mutable files which are frequently updated which increases possibility of merge conflicts
- No locking mechanism
- Concurrency issues, higher possibility of overwriting

### IaC

It stands for Infrastructure as Code. It helps in creating infrastructure from scratch just by defining the desired state you want to obtain. It follows declarative language and uses HCL to define the state.

### What each command does?

init - initializes terraform configurations defined in .tf file
plan - shows what will be implemented in the infrastructure
apply - implements the desired state mentioned in the file
destroy - deletes all resources created using terraform
show - gives all details of current state
state list - lists all the resources being managed by terraform

### What is a state file and why it matters?

State file contains current state of resources that is managed by Terraform. It matters because this is where all metadata, unique ids, details of infrastructure stays.