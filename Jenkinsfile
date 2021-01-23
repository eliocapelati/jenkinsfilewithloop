
abcs = ['a', 'b', 'c']


pipeline {
    agent any


    stages {
        stage('Loop execution') {
            steps {
                echo 'Loop execution'
                recursiveFun(abcs)
                script {
                    def configMap = readJSON file: 'pipelineConfig.json'
                    configMap["environments"].each{ option -> 
                        echo "appname: ${option['appname']}"
                        echo "otherStuff: ${option['otherStuff']}"
                    }
                }
            }
        }
    }
}


@NonCPS
def recursiveFun(elements){
    elements.each{ element -> 
        echo "element: ${element}"
    }
}