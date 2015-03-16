The steps to get andorid source code and build it to a srouces.jar file in Ubuntu
# Steps #

  1. Install curl and git
```
sudo apt-get install curl
sudo apt-get install git-core
```
  1. Download and install repository tool
```
curl http://android.git.kernel.org/repo > repo
sudo chown root repo
sudo chgrp root repo
sudo chmod +x repo
sudo mv repo /usr/local/bin
```
  1. Create a eclair folder for storing full android source code
```
mkdir eclair
cd eclair
```
  1. Initial repository (eclair is 2.1 branch name, use froyo for 2.2)
```
repo init -u git://android.git.kernel.org/platform/manifest.git -b eclair
```
    * this step will take a long time for downloading the source code.
  1. install ant
```
sudo apt-get install ant1.8
```
  1. create a file named build.xml in eclair folder
```
<project name="build-android-src" basedir="." default="build-src">
	<property name="srcfile" value="android-eclair-sources.jar"/>
	<target name="build-src">
		<delete file="${srcfile}"/>
		<jar destfile="${srcfile}">
			<fileset dir="frameworks/base/core/java">
				<include name="**/*.java" />
			</fileset>
			<fileset dir="frameworks/base/graphics/java">
				<include name="**/*.java" />
			</fileset>
			<fileset dir="frameworks/base/location/java">
				<include name="**/*.java" />
			</fileset>
			<fileset dir="frameworks/base/media/java">
				<include name="**/*.java" />
			</fileset>
			<fileset dir="frameworks/base/opengl/java">
				<include name="**/*.java" />
			</fileset>
			<fileset dir="frameworks/base/sax/java">
				<include name="**/*.java" />
			</fileset>
			<fileset dir="frameworks/base/services/java">
				<include name="**/*.java" />
			</fileset>
			<fileset dir="frameworks/base/telephony/java">
				<include name="**/*.java" />
			</fileset>
			<fileset dir="frameworks/base/vpn/java">
				<include name="**/*.java" />
			</fileset>
			<fileset dir="frameworks/base/wifi/java">
				<include name="**/*.java" />
			</fileset>
		</jar>
	</target>
</project>
```
  1. build the script by ant
```
ant
```