pipeline {
      agent any
      stages {
              stage("Cleaning Stage") {
                    steps {
                           bat "mvn clean"
                              }
              }
                              stage("Testing stage") {
                                    steps {
                                         bat "mvn test"
                              }
                              }
                               stage("Packaging stage") {
                                     steps {
                                bat "mvn package"
                               }
                               }
                               stage("docker image") {
                                     steps {
                                bat "docker build -t parinitha456/mavenadd:0.1.RELEASE "
                                bat "docker run -d -t 5000:5000 parinitha456/mavenadd:0.1.RELEASE "
                                bat "docker push parinitha456/mavenadd:0.1.RELEASE"     
                               }
         }
        
      }
}
