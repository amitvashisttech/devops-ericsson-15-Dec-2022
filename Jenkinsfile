pipeline {
    agent any

    environment { 
      repo_url = "https://github.com/amitvashisttech/devops-ericsson-15-Dec-2022.git"
      branch_name = "main"
      project_dir = "03-App-Code/mywebapp/"
      Artifactory-Server-ID = "01"
      Artifactory-Repo = "mywebapp-repo"

    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    
    
    
        stage('Git CheckOut') {
            steps {
                git branch: "${branch_name}", url: "${repo_url}"
            }
        }
    
    
  
        stage('Maven Clean') {
            steps {
                sh "mvn clean -f ${project_dir}/pom.xml"
            }
        }
    
    
    
        stage('Maven Compile') {
            steps {
                sh "mvn compile -f ${project_dir}/pom.xml"
            }
        }
    
    
    
        stage('Maven Test') {
            steps {
                sh "mvn test -f ${project_dir}/pom.xml"
            }
        }
    
    
    
        stage('Maven Package') {
            steps {
                sh "mvn package -f ${project_dir}/pom.xml"
            }
        }

        stage('Archiva') {
            steps {
               archive "${project_dir}/target/*.war"
            }
        }


       stage('Build Management') { 
        steps {
           rtUpload (
              serverId: "${Artifactory-Server-ID}",
              spec: """{ 
                 "files": [
                           {
                              "pattern": "${project_dir}/target/*.war",
                              "target": "${Artifactory-Repo}"
                           }
                         ]
                      }"""
                    )
                }
        }

        stage('Publish Build Info'){ 
          steps { 
                rtPublishBuildInfo (
                    serverId: "${Artifactory-Server-ID}"
                )
            }        
        }



        stage('Docker Compose') {
            steps {
                sh "cd ${project_dir}; docker-compose up -d --build"
            }
        }





   
    }
    
    
    
}

