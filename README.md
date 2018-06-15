Panda Maven Repository
======================

Maven settings.xml
--------------------
	<settings>
		<profiles>
			<profile>
				<id>panda-profile</id>
				<activation>
					<activeByDefault>true</activeByDefault>
				</activation>
				<repositories>
					<repository>
						<id>panda-repo</id>
						<name>Panda Maven Repository</name>
						<url>https://raw.github.com/pandafw/repos/master/</url>
						<layout>default</layout>
						<releases>
							<enabled>true</enabled>
							<updatePolicy>always</updatePolicy>
							<checksumPolicy>warn</checksumPolicy>
						</releases>
						<snapshots>
							<enabled>true</enabled>
							<updatePolicy>daily</updatePolicy>
							<checksumPolicy>warn</checksumPolicy>
						</snapshots>
					</repository>
				</repositories>
			</profile>
		</profiles>
	</settings>

Ivy ivysettings.xml
--------------------
	<ivysettings>
		<settings defaultResolver="default" />
		<resolvers>
			<chain name="public">
				<ibiblio name="maven" m2compatible="true" />
				<ibiblio name="panda" m2compatible="true" root="https://raw.github.com/pandafw/repos/master/" />
			</chain>
		</resolvers>
		<include url="${ivy.default.settings.dir}/ivysettings-shared.xml" />
		<include url="${ivy.default.settings.dir}/ivysettings-local.xml" />
		<include url="${ivy.default.settings.dir}/ivysettings-main-chain.xml" />
		<include url="${ivy.default.settings.dir}/ivysettings-default-chain.xml" />
	</ivysettings>
