
pipeline
{
    agent any
    stages
    {
        stage('Fetch_Project')
        {
            steps
            {
                git 'https://github.com/ChrisKehoe/Jenkins'
            }
        }
        stage('Build_Project')
        {
            steps
            {
                sh label: '', script: 'javac -cp junit-4.13-rc-2.jar:. Student.java studentTest.java'
            }
        }
        stage('Test_Project')
        {
            steps
            {
                sh label: '', script: 'java -cp junit-4.13-rc-2.jar:hamcrest-core-1.3.jar:. org.junit.runner.JUnitCore studentTest'
            }
        }

    }
}
