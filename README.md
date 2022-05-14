# CMPE 172 - Spring Gumball CI/CD

## CI Workflow (Part 1)

Below are screenshots of the proof of the working workflow to trigger a build on push or pull request on the main branch. Here, I updated the README file and triggered a build on push.

![](images/screenshot1.png)

![](images/screenshot2.png)

<br>

## CD Workflow (Part 2)

Below are screenshots of the proof of the working workflow for deployment in GKE.

### Configuring google.yml file in the repo

![](images/screenshot3.png)

### Creating GitHub secret keys

![](images/screenshot4.png)

![](images/screenshot5.png)

![](images/screenshot6.png)

![](images/screenshot7.png)

### Triggering a deployment with release (first try)

![](images/screenshot8.png)

![](images/screenshot9.png)

![](images/screenshot10.png)

![](images/screenshot11.png)

![](images/screenshot12.png)

![](images/screenshot13.png)

There is an error before deployment began. Probably, due to the secret SA key. I have secret key as the private_key that I copied from the JSON file. I will now put the entire JSON secret key file as the secret key on GitHub.

### Triggering a deployment with release (second try)

![](images/screenshot8.png)

![](images/screenshot14.png)

![](images/screenshot15.png)

![](images/screenshot16.png)

![](images/screenshot17.png)

![](images/screenshot18.png)

![](images/screenshot19.png)

![](images/screenshot20.png)

![](images/screenshot21.png)

![](images/screenshot22.png)

![](images/screenshot23.png)

It says that some backend services are in unknown state. Later, we see that in the bottom, it shows that there might be a problem with one of the services. The reason is unknown: could be that the deployment did not go very well because of us or just because GCP is imperfect, or maybe because I am using free trial version of GCP. Nonetheless, it is working:

![](images/screenshot24.png)

