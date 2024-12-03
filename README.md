**Github Repository that contains the rules of the IOCparser project.**

**To use it, follow this instructions :**
  1) Generate an SSH key
      ```
      ssh-keygen -t rsa -b 4096 -C "email@email.com"
      eval "$(ssh-agent -s)"
      ssh-add ~/.ssh/id_rsa
      ```
  2) Add the key to github

     Go in Settings -> SSH and GPG keys -> New SSH Key ;
     
     Add the key in `~/.ssh/id_rsa_github.pub` .
  3) Try to clone the repo

     ```
     git clone git@github.com:arthubhub/osint_rules.git
     ```

**Python BOT configuration**
  1) First, check if Github access is working

     ```
     ssh -T git@github.com
     ```
  2) If the connection doesn't work, verify the SSH key

     ```
     eval "$(ssh-agent -s)"
     ssh-add ~/.ssh/id_rsa
     ```
  3) Tenter de cloner le repo

     ```
     from git import Repo

     repo_url = "git@github.com:arthubhub/osint_rules.git"
     repo_dir = "./repo"
     try:
       repo = Repo.clone_from(repo_url,repo_dir)
       print(f"Dépot cloné dans {repo_dir}")
     except Exception as e:
       print(f"Erreur lors du clonage : {e}")
     ```



     
