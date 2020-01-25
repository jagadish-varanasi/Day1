//test comment
node('master') {
    stage('Git Clone') {
        git branch: 'master', changelog: true, url: 'https://github.com/vjagadishvaranasi/Day1.git'

    }

    stage('Project Name') {
        def projects = readJSON file: "${env.WORKSPACE}/input.json"//has contents o f json

        echo "current workspace is ${env.WORKSPACE}"
        echo "Project name is ${projects.projects.project[0].name}"//first projects refers to above variable.and second project is of input.json
    }
    
    stage('RUN Python Script') {
        bat "hello-nmit.py"//sh refers to command script
        bat "/hello-nmit.py"
    }

}
