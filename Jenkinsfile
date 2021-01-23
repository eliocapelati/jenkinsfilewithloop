
abcs = ['a', 'b', 'c']
def configMap = readJSON file: 'pipelineConfig.json'

pipeline {
    agent any

    stages {
        stage('Loop execution') {
            steps {
                echo 'Loop execution'
                recursiveFun(abcs)
            }
        }
    }
}


@NonCPS
def recursiveFun(elements){
    elements.each{ element -> 
        echo "element: ${element}"
    }

    configMap["environments"].each{ option -> 
        echo "appname: ${option['appname']}"
        echo "otherStuff: ${option['otherStuff']}"
    }
}