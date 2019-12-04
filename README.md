# eip

[![Build Status](https://drone.techservices.illinois.edu/api/badges/techservicesillinois/terraform-aws-eip/status.svg)](https://drone.techservices.illinois.edu/techservicesillinois/terraform-aws-eip)

Provides an Elastic IP resource.

Argument Reference
-----------------

The following arguments are supported:

* `name` - (Required) Name for the EIP resource.
* `vpc` - (Optional) Boolean if the EIP is in a VPC or not.
* `instance` - (Optional) EC2 instance ID.
* `network_interface` - (Optional) Network interface ID to associate with.
* `associate_with_private_ip` - (Optional) A user specified primary or secondary private IP address to associate with the Elastic IP address. If no private IP address is specified, the Elastic IP address is associated with the primary private IP address.
* `tags` - (Optional) A mapping of tags to assign to the resource.
* `public_ipv4_pool` - (Optional) EC2 IPv4 address pool identifier or amazon. This option is only available for VPC EIPs.

Attributes Reference
--------------------

In addition to all arguments above, the following attributes are exported:

* `id` - Contains the EIP allocation ID.
* `public_ip` - Contains the public IP address.
* `public_dns` - Public DNS associated with the Elastic IP address.

Credits
--------------------

**Nota bene:** The vast majority of the verbiage on this page was
taken directly from the Terraform manual, and in a few cases from
Amazon's documentation.
