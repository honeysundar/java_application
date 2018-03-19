#!/usr/bin/env groovy

// app defns per env, now have only one (dev)

node {
  def pipeline = new cicd.Pipeline();
  def testRunner
  def image
  String imageName

  stage('Prepare Pipeline') {
    // Prepare the workspace
    pipeline.cleanupAndCheckout();
  }
}
