# gradle-scripts
Some scripts for Gradle.

## eclipse-project-filter.gradle

Adds eclipse project filter. Allows to hide gradle subprojects or build directory.

Example, usage:

	def getEclipseFilter() {
		return '1.0-projectRelativePath-matches-true-true-(subproject-.*|test|build)'
	}
	
	apply from: "https://raw.githubusercontent.com/Schnitker/gradle-scripts/master/eclipse-project-filter.gradle"
	

## eclipse-project-libsort.gradle

Sorts the eclipse classpath (libraries). The result is a sorted Eclipse project/package explorer view.

Usage:

	apply from: "https://raw.githubusercontent.com/Schnitker/gradle-scripts/master/eclipse-project-libsort.gradle"

## eclipse-project-utf8.gradle

Adds default utf-8 encoding for eclipse project.

Usage:

	apply from: "https://raw.githubusercontent.com/Schnitker/gradle-scripts/master/eclipse-project-utf8.gradle"

## eclipse-project-nature.gradle

Adds gradle nature to eclipse project. The eclipse plugin "buildship 1.0.2" is required.
Allows to use standard 'gradlew cleanEclipse eclipse' command, without destroying gradle project nature.

Usage:

	apply from: "https://raw.githubusercontent.com/Schnitker/gradle-scripts/master/eclipse-project-nature.gradle"
