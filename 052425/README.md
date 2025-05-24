# 5/24/25 Saturday Class 6.5 Notes

## Basic Configuration Assumed
1) Terraform authenticated and successfully initalized 
2) GCS Remote backend bucket in use
3) Google Provider with region default set
4) Web server startup shell script
5) gitignore file

## Resources Assumed
- 1 google_compute_network
- 1 google_compute_subnetwork
- 1 google_compute_router
- 1 google_compute_router_nat
- 3 google_compute_firewall

## Documentation
1) VM Docs
  - [Terraform Registry for VM Resource](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/compute_instance)
  - [REST API Documentation](https://cloud.google.com/compute/docs/reference/latest/instances)

2) Template Docs
  - [Terraform Registry for Regional Instance Template](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/compute_region_instance_template)
  - [REST API Documentation](https://cloud.google.com/compute/docs/reference/rest/v1/regionInstanceTemplates)

## Plan
1) Review Architecture
2) Encourage clean network architecture
3) Build out VM instance
4) Build out instance template with VM instance parameters