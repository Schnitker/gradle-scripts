# gradle-scripts
Some scripts for Gradle.

## eclipse-project-filter.gradle

Adds eclipse project filter. Allows to hide gradle subprojects or build directory.

Example:

	def getEclipseFilter() {
		return '1.0-projectRelativePath-matches-true-true-(subproject-.*|test|build)'
	}
	
	apply from: "eclipse-project-filter.gradle"
	

## eclipse-project-libsort.gradle

Sorts the eclipse classpath (libraries). The result is a sorted Eclipse project/package explorer view.

Example:

	apply from: "eclipse-project-libsort.gradle"

## eclipse-project-nature.gradle

Adds default utf-8 encoding for eclipse project.

Example:

	apply from: "eclipse-project-nature.gradle"

## eclipse-project-utf8.gradle

Adds gradle nature to eclipse project. The eclipse plugin "buildship 1.0.2" is required.
Allows to use standard 'gradlew cleanEclipse eclipse' command, without destroying gradle project nature.

Example:

	apply from: "eclipse-project-utf8.gradle"
