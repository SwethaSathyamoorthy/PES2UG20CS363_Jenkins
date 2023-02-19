pipeline
{
    agent any
    stages
    {
        stage ('Build')
        {
            steps
            {
                sh 'g++ pes2ug20cs363_5.cpp -o pes2ug20cs363_5'
                echo 'build stage successful'
                build job: 'PES2UG20CS363-1'
            }
        }
        stage ('Test')
        {
            steps
            {
                sh './pes2ug20cs363_5'
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
