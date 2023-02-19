pipeline
{
    agent any
    stages
    {
        stage ('Build')
        {
            steps
            {
                sh 'g++ PES2UG20CS363_5.cpp -o PES2UG20CS363_5'
                echo 'build stage successful'
                build job: 'PES2UG20CS363-1'
            }
        }
        stage ('Test')
        {
            steps
            {
                sh './PES2UG20CS363_5'
                echo 'test stage successful'
            }
        }
        stage ('Deploy')
        {
            steps
            {
                echo 'deployment successful'
            }
        }
    }
    post
    {
        failure
        {
            echo 'pipeline failed'
        }
    }
}
