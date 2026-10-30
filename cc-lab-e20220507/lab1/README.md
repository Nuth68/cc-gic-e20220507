# Cloud Lab 1 Submission — Amazon EC2


- **Student name: PRAVE  Vinuth**
- **Student ID: e20220507**
- **Learner Lab user name: voclabs/user5622990=PRAVE_VINUTH**
- **Date completed: Sat 24 Oct**

---

## Part 1.1 — An Amazon EC2 Walkthrough

### Security group

![Security group inbound rules](images/01-security-group.png)

### Key pair

![Key pair](images/02-key-pair.png)

### Instance details

![Instance details](images/03-instance-details.png)

### Browser test

![Browser test](images/04-browser-test.png)

### SSH connection

![SSH connection](images/05-ssh-connection.png)

Did you connect with your own SSH client or with EC2 Instance Connect?

---

## Part 1.2 — EC2 Web Solution (Challenge)

### Launch configuration

![Launch configuration](images/06-challenge-launch.png)

### Security group

![Challenge security group](images/07-challenge-security-group.png)

### Running instance

![Challenge instance](images/08-challenge-instance.png)

### Commands on the instance

![Terminal commands—installation](images/09-challenge-terminal.png)
![Terminal commands—installation complete](images/09-challenge-terminal-2.png)
![Terminal commands—Apache status](images/09-challenge-terminal-3.png)

Paste the commands you ran to install the web server and create `index.html`:

```bash
sudo yum update -y
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
sudo systemctl status httpd
echo '<!DOCTYPE html>
<html>
<head>
    <title>EC2 Challenge</title>
</head>
<body>
    <h1>Welcome to the EC2 Challenge</h1>
</body>
</html>' | sudo tee /var/www/html/index.html

```

### Browser test

![Welcome to the EC2 Challenge](images/10-challenge-browser.png)

---

Clean up
 - [✓]Part 1.1: instance terminated, key pair and security group deleted.
 - [✓]Part 1.2: instance terminated, security group (and key pair, if any) deleted.