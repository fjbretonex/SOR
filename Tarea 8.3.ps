function Try-UO ($UniOrg) {
# Verificamos si existe nuestra unidad organizativa, y sino es así la creamos
if (Get-ADOrganizationalUnit -filter 'Name -like $UniOrg')
	{
    write-host "La unidad organizativa $UniOrg existe, seguimos con la ejecución..."
  }
  else
  {
    write-host "La unidad organizativa $UniOrg no existe, vamos a proceder a su creación..."
    New-ADOrganizationalUnit -Name "$UniOrg" -Path "DC=SOR,DC=LOCAL"
    write-host "Unidad organizativa $UniOrg creada"
  }
}


function New-Usuario ($nombre,$usuarios,$UniOrg) {
		for ($i=1; $i -le $usuarios ; $i++){
				if ($i -lt 10)
					{
					 $indice="0$i"
				 }
					else
				{
						$indice=$i
				}
				# Instrucción que crea los usuarios
					New-ADUser -Name $nombre-$indice -GivenName $nombre-$indice -Path “OU=$UniOrg,DC=SOR,DC=local” -accountPassword (ConvertTo-SecureString -AsPlainText “p@ssw0rd” -Force)
				# Ahora aprovechamos y activamos el usuario
					Enable-ADAccount -Identity $nombre-$indice
				# Mensaje de confirmación de creación
					write-host "Creado el usuario $nombre-$indice y habilitado"
		}
		# Mensaje que indica que hemos finalizado correctamente
		echo "" "Proceso de creación de usuarios finalizado correctamente"
}

function New-Equipo ($CadenaEquipo,$NumEquipos,$UnidOrg) {
	# Procedemos a crear los equipos utilizando un bucle for
	for ($i=1; $i -le $NumEquipos ; $i++){
			# Instrucción que crea los equipos
			New-ADComputer -Enabled $true -Name "$CadenaEquipo-$i" -Path “OU=$UnidOrg,DC=SOR,DC=local” -SAMAccountName "$CadenaEquipo-$i"
			# Ahora aprovechamos y activamos el usuario
			Get-ADComputer $CadenaEquipo-$i | Set-ADComputer -Enabled $true
			# Mensaje de confirmación de creación
			write-host "Creado el equipo $CadenaEquipo-$i y habilitado"
	}
	# Mensaje que indica que hemos finalizado correctamente
	write-host "" ;"Proceso de creación de equipos finalizado correctamente."; ""
}
