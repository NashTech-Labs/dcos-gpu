### What will this role do ?

The above ansible role will install kernel devel in the machines where it will be run.

THis gpu role first checks for the kernel devel and then further installs it from the install_gpu.sh script.

So in the script first it will blacklist nvidia conflicting kernel modules and further it will install cuda driver.

#### Variable used in the install_gpu.sh.

- PRIVATE_DEPLOYMENT=" pass your value ( true or false) "
- S3_ENDPOINT= " pass the s3 enpoint value "
- VULKAN_FILE_PATH= " pass the vulkan file path "


### How to run the playbook .

To run the playbook follow the below command:-

`ansible-playbook -i <your inventory file> playbook.yml`

**Note**:-  If you are running on your local system then you don't need to pass inventory file. Just use localhost in hosts of playbook. 