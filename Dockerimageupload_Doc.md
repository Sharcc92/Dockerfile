# Getting an image to Docker Hub [Link]
1. Imagine you made your own Docker image and would like to share it with the world you can sign up for an account on https://hub.docker.com/. After verifying your email you are ready to go and upload your first docker image.
2. Log in on https://hub.docker.com/ (if you do not have an account create one)
3. Click on Create Repository
4. Choose a name (e.g. soncreo) and a description for your repository and click Create.
5. Log into the Docker Hub from the command line 
    ```
    docker login --username=yourhubusername -
    ```
    Enter your password when prompted. Then you should get the message `Login Succeeded`.
6. Save an existing docker image
    Check the image ID using: `docker images`

    and what you will see will be similar to
    
    ```

    REPOSITORY                                        TAG                 IMAGE ID            CREATED             SIZE
    sharcc92/soncreov2                                latest              12cb16f7b0d3        15 minutes ago      88.1MB
7. Tag your image (save with an new name in the form `yourhubusername/respositoryname:newtag`.
    ```
    docker tag bb38976d03cf yourhubusername/verse_gapminder:firsttry
    ```
    The number must match the image ID and :newtag is the tag. In general, a good choice for a tag is something that will help you understand what this container should be used in conjunction with, or what it represents. If this container contains the analysis for a paper, consider using that paper’s DOI or journal-issued serial number; if it’s meant for use with a particular version of a code or data version control repo, that’s a good choice too - whatever will help you understand what this particular image is intended for.
8. Push your image to the repository you created
    ```
    docker push yourhubusername/verse_gapminder
9. Successful finished. Docker image can be publically downloaded by searching in [Dockerhub].
    
[Link] https://ropenscilabs.github.io/r-docker-tutorial/04-Dockerhub.html
[Dockerhub] https://hub.docker.com/

