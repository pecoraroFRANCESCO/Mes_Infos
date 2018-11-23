# Comment créer un script qui permet d'afficher mes fichiers cachés

1. Dans Automator 
Choisir Processus > Exécuter un script AppleScript
2. Remplire le script

```
try
	set state to do shell script "defaults read com.apple.finder AppleShowAllFiles" as string
	if state is "0" then
		do shell script "defaults write com.apple.finder AppleShowAllFiles -bool TRUE"
	else
		do shell script "defaults write com.apple.finder AppleShowAllFiles -bool FALSE"
	end if
end try
tell application "Finder" to quit
delay 1
tell application "Finder" to launch
```
SOURCE: [https://gist.github.com/jpoehls/2998520](https://gist.github.com/jpoehls/2998520)



