# Ansible + Jenkins CI/CD Pipeline 🚀

> One git push. Every server configured. Zero manual steps.

---

## What This Does

A fully automated CI/CD pipeline that provisions, configures, and deploys a web application across multiple AWS EC2 servers — triggered by a single Jenkins pipeline.

```
Git Push → Jenkins → Ansible → EC2 Servers → Live App ✅
```

---

## Stack

| Tool | Purpose |
|------|---------|
| **Jenkins** | CI/CD pipeline trigger |
| **Ansible** | Server configuration & automation |
| **Ansible Vault** | Secrets encryption |
| **geerlingguy.*** | Pre-built Galaxy roles |
| **Docker** | Container management |
| **MySQL** | Database setup |
| **AWS EC2** | Cloud infrastructure |

---

## What Gets Automated

- ✅ EC2 servers provisioned (control + targets)
- ✅ MySQL installed & configured
- ✅ Docker set up across all servers
- ✅ Static website deployed & connected to database
- ✅ DB credentials encrypted with Ansible Vault
- ✅ Everything triggered on every git push

---

## Project Structure

```
ansible-jenkins/
├── ansible.cfg
├── inventory/
│   └── hosts
├── roles/
│   ├── mysql/
│   ├── docker/
│   └── website/
├── playbook.yaml
├── Jenkinsfile
└── vault/
    └── secret.yml
```

---

## Quick Start

**1. Clone the repo:**
```bash
git clone https://github.com/Ahad9049/ansible-jenkins-pipeline.git
cd ansible-jenkins-pipeline
```

**2. Set permissions on PEM file:**
```bash
chmod 400 ~/k8s.pem
```

**3. Update inventory:**
```bash
nano inventory/hosts
```

**4. Create Ansible Vault:**
```bash
ansible-vault create vault/secret.yml
```

**5. Run manually:**
```bash
ansible-playbook playbook.yaml --ask-vault-pass
```

**6. Or let Jenkins handle it:**
```
Push to GitHub → Jenkins auto-triggers → Done ✅
```

---

## Key Concepts Used

**geerlingguy.*** — battle-tested Galaxy roles, no reinventing the wheel
**community.*** — official collections for flexible, scalable automation
**Ansible Vault** — secrets never exposed in plain text

---

## Author

**Abdul Ahad** — [@Ahad9049](https://github.com/Ahad9049)

⭐ Star this repo if it helped you!
