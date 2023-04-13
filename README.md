# task 7
## the purpose of this task was to *create my first CI/CD pipeline* and *understand the principles of the CI/CD practice*
1. first thing what I did according to the instruction, I have create a *Service Account for Terraform* by going to *GCP Console* --> *IAM* and clicking **"Create Service Account**
2. the name can be no matter what kind, I chose: **dareit-vm-tf-ci**, for role I chose = *Project --> Editor*, then I clicked *Continue*, the rest is not so important so I skipped the granting additional users access and clicked **Done**
3. after this, I have generated a *Key* for that Service Account by clicking **ADD KEY** and chose **JSON for the Key** --> this key is used as a secret variable in my pipeline, and for that I modified it by modifing the content of the *json file* (by removing all new line characters from the file)
4. for that I used the command:
```
vim your-file-name.json
```
5. and:

Press **:**

Type: **%s;\\n; ;g** and press *enter*

Press **:**

and saved the file by typing **wq!**

6. in the next step, I have created a bucket were I am storing the terraform state file
7. afterwards, I have created new repository in Github with the name *dareit-task-terraform*
8. in the *Settings* tab I chose **Actions** under the *Security section* and clicked in the button ***New repository secret*** where I pasted the content of *my-file-name.json* (which was modified)
9. in addition I named the secret as *TF_GOOGLE_CREDENTIALS*
10. I am going back to my terminal and after adding [*mainf.tf*](https://github.com/inspiritgoldenx/dareit-task-terraform/blob/main/main.tf) I am also adding [*backend.tf*](https://github.com/inspiritgoldenx/dareit-task-terraform/blob/main/backend.tf) then I have created [*provider.tf*](https://github.com/inspiritgoldenx/dareit-task-terraform/blob/main/provider.tf)
