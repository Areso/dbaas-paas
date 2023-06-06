# DBAAS and PAAS
It's a service description, where I announce and describe the service endpoints  
The service serves is a middleware for running playbooks from  
https://github.com/Areso/Webinar-ansible  
and others playbook repos  

## Endpoints of the service
`/vm_create`  
body:  
  "name":vm_name  
  "size":vm_size - optional  
  "region":region_slug - optional  
  
`/software_install`  
body:  
  "name":vm_name  
  
`/vm_delete`  
body:  
  "name":vm_name  
  
`/pg_install`  
body:  
  "name":vm_name  
  "dbname":dbname  
  "username":username  
  "password":password  
  
return asnwer:  
  "task_id":int  
  
`/get_pg_details`  
body:  
  "task_id":int

## TODO list:
add MySQL install endpoint    
add backup endpoint  
add `/check_db_size` endpoint  
add `/check_all_db_sizes` endpoint  
