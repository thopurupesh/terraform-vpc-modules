<h1>Terraform VPC</h1>
<h2>What Do We Achieve with This?</h2>
<ol type="1">
<li>Create vpc with CIDR block 10.0.0.0/16                                        </li>
<li>Create public subnet in above vpc with CIDR block 10.0.1.0/24                 </li>
<li>Create private subnet in above vpc with CIDR block 10.0.2.0/24                </li>
<li>Create and Assign Internet Gateway and Public Route Table to the Public Subnet</li>
<li>Create and Assign Private Route Table to the Private Subnet                   </li>
<li>Create the Security Group for the Public and Private Subnet                   </li>
<li>Create SSH Key pair for the EC2 instances                                     </li>
<li>Create EC2 instances and install Apache on webserver                          </li>
</ol>

<h2>Implementation:</h2>
<ol type="1">
<li>Download the cloud.tf and vars.tf file.                                                                                          </li>
<li>Replace the access_key, secret_key and key file values in the files.                                                             </li>
<li>Generate the .PEM, .ppk files and place in the same location as cloud.tf and vars.tf.                                            </li>
<li>On a linux machine, execute the following                                                                                   </li>
<p>ssh-keygen -y -f .pem</p><li>Copy the output and paste it in a empty file and this will be <Your_Key>. Maintain this in the same directory as other .tf files.</li>
<li>Execute below commands.<p>terraform plan <br />
terraform apply -auto-approve</p>
</ol>
