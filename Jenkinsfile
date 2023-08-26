pipeline {
agent{ label 'dotnet6'}
triggers { pollSCM('* * * * *') }
stages{
stage('vcs'){
steps{
 git branch:'main',
url:'https://github.com/jenkinsaugest/MusicStore.git'
}
}
stage('build') {
steps{
 sh 'dotnet restore ./MusicStore/MusicStore.csproj'
}
 }
stage ('dotnet test'){
 steps{
sh 'dotnet test ./MusicStoretest/MusicStoretest.csproj'
}
}
}
}




        
