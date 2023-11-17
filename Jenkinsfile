pipeline {
    agent any
    environment {
        PLAYBOOK = '' #Enter the Playbook_location
        TESTING_INVENTORY = '' #Enter the Testing inventory location
        PRODUCTION_INVENTORY = '' # Enter the Prod inventory location
    }
    stages {
        stage('Deploy to Testing') {
            steps {
                ansiblePlaybook(
                    playbook: '${PLAYBOOK}',
                    inventory: '${TESTING_INVENTORY}',
                    extras: '-e environment=testing'
                )
            }
        }
        stage('Deploy to Production') {
            steps {
                ansiblePlaybook(
                    playbook: '${PLAYBOOK}',
                    inventory: '${PRODUCTION_INVENTORY}',
                    extras: '-e environment=production'
                )
            }
        }
    }
}
