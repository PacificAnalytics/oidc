# How to compile extension for PhenoTips #

This description is for the original OIDP repo.

Open the pom.xml and add necessary dependencies:

	 <repositories>
	    <repository>
	      <id>xwiki</id>
	     <name>Xwiki maven Releases</name>
	    <url>http://maven.xwiki.org/releases/</url>
	  </repository>
	  <repository>
	    <id>externals</id>
	    <name>XWiki maven externals</name>
	    <url>http://maven.xwiki.org/externals/</url>
	  </repository>
	  <repository>
	    <id>PhEd</id>
	    <name>PhEdUk</name>
	    <url>https://www2.ph.ed.ac.uk/maven2/</url>
	  </repository>
	</repositories>
		
Change the version of the parent to align with Xwiki version used by PhenoTips.

	<parent>
	  <groupId>org.xwiki.contrib</groupId>
	  <artifactId>parent-platform</artifactId>
	  <version>7.4-6</version>
	</parent>

`7.4-6` aligns with `PhenoTips 1.4-SNAPSHOT`

Buil the plugin and copy the target plus these jars to PhenoTips WEB-INF/lib

	nimbus-jose-jwt-4.18.jar
	oauth2-oidc-sdk-5.10-xwiki.jar
	json-smart-1.3.1.jar
	
