Membuat AMI bernama devops-ec2-ami dari EC2 instance yang sudah ada bernama devops-ec2 di region us-east-1 menggunakan Terraform, dengan memastikan AMI berada dalam status available. Konfigurasi ditulis dengan mengupdate file main.tf di direktori /home/bob/terraform

Update File main.tf


Di direktori /home/bob/terraform, update file main.tf dengan konten berikut:


Penjelasan:


provider “aws”: Mengatur region AWS ke us-east-1.


data “aws_instance”: Mengambil data instance devops-ec2 berdasarkan tag Name.


aws_ami_from_instance: Membuat AMI devops-ec2-ami dari instance devops-ec2.


tags: Menambahkan tag Name = 
“devops-ec2-ami” untuk identifikasi.


Jalankan Terraform init, plan, apply


