
abcs = ['a', 'b', 'c']

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
        sh "element: ${element}"
    }
}