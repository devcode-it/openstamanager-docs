# Documentazione dei progetti DevCode

Questa repository contiene i file che formano l'applicazione ufficiale del gestionale OpenSTAManager.

<!-- TOC depthFrom:2 depthTo:6 orderedList:false updateOnSave:true withLinks:true -->

- [Windows](#windows)
- [Testing](#testing)

<!-- /TOC -->

## Windows

I passaggi necessari per la compilazione dei sorgenti sono i seguenti:
- [Installare Chocolatey](https://chocolatey.org/install) da Amministratori
    ```bash
    @"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
    ```
- Installare Ruby e msys2 con chaintool:
    ```bash
    choco install ruby -y
    choco install msys2 -y
    ```
- Installare Jekyll e Bundler:
    ```bash
    gem install jekyll bundler
    ```

E' quindi necessario eseguire il seguente comando nella cartella della documentazione:
 ```bash
bundle install
```

## Testing

Sono disponibili i seguenti comandi per semplificare il testing:
```bash
npm run serve         # Avvia Jekyll in locale (http://localhost:4000/)
```
