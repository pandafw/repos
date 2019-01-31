 Panda Maven Repository
========================

Maven pom.xml
--------------------
	<repositories>
		<repository>
			<id>panda</id>
			<url>https://pandafw.github.io/repos/panda/</url>
		</repository>
	</repositories>

Ivy ivysettings.xml
--------------------
	<ivysettings>
		<settings defaultResolver="default" />
		<resolvers>
			<chain name="public">
				<ibiblio name="maven" m2compatible="true" />
				<ibiblio name="panda" m2compatible="true" root="https://pandafw.github.io/repos/panda/" />
			</chain>
		</resolvers>
		<include url="${ivy.default.settings.dir}/ivysettings-shared.xml" />
		<include url="${ivy.default.settings.dir}/ivysettings-local.xml" />
		<include url="${ivy.default.settings.dir}/ivysettings-main-chain.xml" />
		<include url="${ivy.default.settings.dir}/ivysettings-default-chain.xml" />
	</ivysettings>
