node {
	def app

	stage("Pulling from git") {
		git "https://github.com/shaong/jdockert.git"
	}

	stage("Build docker image") {
		// param: output-image-name
		app = docker.build("jdockert")
	}

	stage("Test image") {
		app.inside {
			sh "uname -a"
		}
	}
}
