all: TShockAPI/bin/Release/TerrariaServer.exe
	@cp ./TShockAPI/bin/Release/* Output/
	@cp ./prebuilts/* Output/
	@mkdir -p ./Output/ServerPlugins
	@mv ./Output/TShockAPI.dll ./Output/ServerPlugins/


TShockAPI/bin/Release/TerrariaServer.exe: TerrariaServerAPI/TShock.Modifications.Bootstrapper/bin/Release/Output/OTAPI.dll 
	@msbuild /p:Configuration=Release /p:ConfigurationName=Release ./TShock.sln

TerrariaServerAPI/TShock.Modifications.Bootstrapper/bin/Release:
	@ln -s ../../.nuget/packages ./TerrariaServerAPI/packages
	@msbuild ./TerrariaServerAPI/TShock.4.OTAPI.sln /p:Configuration=Release

TerrariaServerAPI/TShock.Modifications.Bootstrapper/bin/Release/Output/OTAPI.dll: TerrariaServerAPI/TShock.Modifications.Bootstrapper/bin/Release
	@mkdir -p TerrariaServerAPI/TShock.Modifications.Bootstrapper/bin/Release/Output
	@mono TerrariaServerAPI/TShock.Modifications.Bootstrapper/bin/Release/TShock.Modifications.Bootstrapper.exe -in TerrariaServerAPI/TShock.Modifications.Bootstrapper/bin/Release/OTAPI.dll \
		-mod="TerrariaServerAPI/TShock.Modifications.**/bin/Release/TShock.Modifications.*.dll" \
		-o=TerrariaServerAPI/TShock.Modifications.Bootstrapper/bin/Release/Output/OTAPI.dll
clean:
	rm -f TerrariaServerAPI/packages
	rm -rf TerrariaServerAPI/TShock.Modifications.Bootstrapper/bin
	# @msbuild ./TShock.sln -target:Clean
	# @msbuild ./TerrariaServerAPI/TShock.4.OTAPI.sln -target:Clean
