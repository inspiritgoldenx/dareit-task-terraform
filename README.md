# task 7 👽🚀
## the purpose of this task was to *create my first CI/CD pipeline* and *understand the principles of the CI/CD practice*
1. first thing what I did according to the instruction, I have create a *Service Account for Terraform* by going to *GCP Console* --> *IAM and Admin* and clicking **Service Account** --> **Create Service Account**
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
10. I am going back to my repository and after adding [*mainf.tf*](https://github.com/inspiritgoldenx/dareit-task-terraform/blob/main/main.tf) I am also adding [*backend.tf*](https://github.com/inspiritgoldenx/dareit-task-terraform/blob/main/backend.tf) then I have created [*provider.tf*](https://github.com/inspiritgoldenx/dareit-task-terraform/blob/main/provider.tf)
11. next, I have created: a file in my repository named: **.github/workflows/terraform.yml** with [*terraform.yml*](https://github.com/inspiritgoldenx/dareit-task-terraform/blob/main/.github/workflows/terraform.yml) where all of the above files were added
12. ufff 
13. then I have commited all files to the repo and pushed the change to my remote repository, so in the *Actions tab* I can see the workflows
14. by clicking on the *Terraform Job* I see the details of it, in addition in the *GCP Console* a new Compute Instance got created 🎉
![dareITterraformzad7](https://user-images.githubusercontent.com/125319277/231847471-524a9dac-339e-4616-8ab5-3c22521da57b.jpg)

![dareITzad7](https://user-images.githubusercontent.com/125319277/231847766-e297c0fe-77f6-46d5-aec9-6957a51795b2.jpg)
