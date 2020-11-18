# สร้าง server ของตัวเองบนครื่อง VM ware 
เมื่อสร้างเสร็จแล้ว ให้ลง Jenkins&Docker 
วิธีการลง Docker
คำสั่ง
sudo apt install docter.io
docker --version 

วิธีการลง Jenkins
sudo apt install jenkins.io
jenkins --version

Pull jenkins image from docker hub
docker run Jenkins


Create a new volume on docker host to keep jenkins configurations
mkdir ~/myJenkinsVolume


Run jenkins container in detached mode
docker run -d -p 8888:8080 -p 50000:50000 --restart=always --name devopsjenkins -v ~/myJenkinsVolume:/var/jenkins_home -t -u root jenkins


