```powershell
 if (-Not(Test-Path $profile) -Or (Select-String -Path $profile -pattern npmplease) -eq $null) { Add-Content $profile "function npmplease { rm -r .\node_modules; rm .\package-lock.json ; npm install };" }
 ```


Stores the function `npmplease` in current user profile so it will be available in all future powershell sessions. Checks to not add it twice.
