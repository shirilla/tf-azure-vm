## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.0 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | >= 3.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | >= 3.0 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [azurerm_dns_a_record.record](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/dns_a_record) | resource |
| [azurerm_linux_virtual_machine.vm](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/linux_virtual_machine) | resource |
| [azurerm_network_interface.networkInterface0](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/network_interface) | resource |
| [azurerm_public_ip.publicIp1](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/public_ip) | resource |
| [azurerm_resource_group.rg](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/resource_group) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_admin_user"></a> [admin\_user](#input\_admin\_user) | The admin username for the Linux VM. | `string` | n/a | yes |
| <a name="input_assign_public_ip"></a> [assign\_public\_ip](#input\_assign\_public\_ip) | Boolean flag to determine if a public IP should be assigned to the VM. | `bool` | `false` | no |
| <a name="input_az_location"></a> [az\_location](#input\_az\_location) | The Azure region where all resources will be deployed (e.g., eastus, westus2). | `string` | n/a | yes |
| <a name="input_init_script_path"></a> [init\_script\_path](#input\_init\_script\_path) | Path to the initialization (cloud-init) script to be run on VM creation. | `string` | `""` | no |
| <a name="input_public_dns_zone_name"></a> [public\_dns\_zone\_name](#input\_public\_dns\_zone\_name) | The name of a pre-existing public DNS zone that the VM will be assigned to. If assign\_public\_ip=false, this variable should not be set. | `string` | `""` | no |
| <a name="input_public_dns_zone_rg"></a> [public\_dns\_zone\_rg](#input\_public\_dns\_zone\_rg) | The resource group name of a pre-existing public DNS zone that the VM will be assigned to. If assign\_public\_ip=false, this variable should not be set. | `string` | `""` | no |
| <a name="input_public_ip_allocation_method"></a> [public\_ip\_allocation\_method](#input\_public\_ip\_allocation\_method) | Public address is Dynamic or Static address | `string` | n/a | yes |
| <a name="input_rg_name"></a> [rg\_name](#input\_rg\_name) | The name of the Azure Resource Group in which resources will be created. | `string` | n/a | yes |
| <a name="input_servername"></a> [servername](#input\_servername) | The name of the Linux virtual machine to be created. | `string` | n/a | yes |
| <a name="input_size"></a> [size](#input\_size) | The size (SKU) of the Azure Linux VM (e.g., Standard\_B1s, Standard\_DS1\_v2). | `string` | n/a | yes |
| <a name="input_ssh_public_key_path"></a> [ssh\_public\_key\_path](#input\_ssh\_public\_key\_path) | Path to the SSH public key file to be added for admin access to the VM. | `string` | n/a | yes |
| <a name="input_subnet_id"></a> [subnet\_id](#input\_subnet\_id) | The ID of the subnet to which the VM will be attached (e.g., /subscriptions/xxxx/resourceGroups/xxx/providers/Microsoft.Network/virtualNetworks/xxx/subnets/xxx). | `string` | n/a | yes |
| <a name="input_tags"></a> [tags](#input\_tags) | A map of tags to assign to all resources. These will be merged with module-defined tags. | `map(string)` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_private_ip_address"></a> [private\_ip\_address](#output\_private\_ip\_address) | The private IP address of the VM. |
| <a name="output_private_nic_id"></a> [private\_nic\_id](#output\_private\_nic\_id) | The ID of the private network interface. |
| <a name="output_public_ip_address"></a> [public\_ip\_address](#output\_public\_ip\_address) | The public IP address of the VM (if assigned). |
| <a name="output_resource_group_name"></a> [resource\_group\_name](#output\_resource\_group\_name) | The name of the resource group. |
| <a name="output_vm_id"></a> [vm\_id](#output\_vm\_id) | The ID of the Linux virtual machine. |
| <a name="output_vm_name"></a> [vm\_name](#output\_vm\_name) | The name of the Linux virtual machine. |
