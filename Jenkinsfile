#!/usr/bin/env groovy

pipeline {
	agent none
	stages {
	    stage('codestyles') {
	    	agent { docker 'joomlaprojects/docker-phpcs' }
	    	steps {
	    	    sh "phpcs --report=full --extensions=php -p --standard=build/phpcs/Joomla ."    
	    	}
	    	
	    }
	    stage('test') {
	        steps {
	            sh "echo stage test"    
	        }
	        
	    }
	
	}
}