# Creating a AWS EC2 Instance
resource "aws_instance" "server-instance" {
  # Define number of instance
  instance_count = var.number_of_instances
 
  # Instance Configuration
  ami                    = var.ami
  instance_type          = var.instance_type
  subnet_id              = var.subnet_id
  vpc_security_group_ids = var.security_group
 
  # Instance Tagsid
  tags = {
    Name = "${var.instance_name}"
  }
}

<!---
TanzeelCyber/TanzeelCyber is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
