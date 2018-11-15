node {
 
 stage("Checkout") {
        checkout scm
      } 
  
 stage("Project Build") {
        sh "mvn clean package" 
        // TODO: specify how you would build your project
        //
        // @example ---------------------------
        // sh "rm -rf ./node_modules/*"
        // sh "npm install"
        // sh "npm install -g webpack"
        // sh "webpack --config webpack.config.${wepackCfg}.js --progress"
      }

      stage("Docker build") {
        // sh "cp -r  ~/certs ."
        //  TODO: replace the ecr (repo) with the right repo name.
       sh "docker build -t java_app ."
      }
 
}
