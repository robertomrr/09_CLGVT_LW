# Objetivo desta aplicação

Servir de referencia para criação de aplicações utilizando o Livewire3

## Links

    https://www.youtube.com/watch?v=e83fM_0mGa8&t=133s
    https://livewire.laravel.com/docs/quickstart
    https://github.com/lucascudo/laravel-pt-BR-localization

    https://www.youtube.com/@yelocode/featured
    https://github.com/yelocode/livewire3-datatable/tree/main

## Criar Aplicação

    > composer create-project --prefer-dist laravel/laravel 09_CLGVT_LW
    > cd 09_CLGVT_LW
    > git init
    > git add .
    > git commit -m "First Commit"
    > npm install

## Instalação do Breeze (livewire)

Laravel Breeze é uma implementação mínima e simples de todos os recursos de autenticação do Laravel , incluindo:
 login, registro, redefinição de senha, verificação de e-mail e confirmação de senha.
 Além disso, o Breeze inclui uma página simples de “perfil” onde o usuário pode atualizar seu nome, endereço de e-mail e senha

 > composer require laravel/breeze --dev
 > php artisan breeze:install
    Which Breeze stack would you like to install?
        Blade with Alpine .................................................................... blade
        Livewire (Volt Class API) with Alpine ................................................ livewire
        Livewire (Volt Functional API) with Alpine ........................................... livewire-functional
        React with Inertia ................................................................... react
        Vue with Inertia ..................................................................... vue
        API only ............................................................................. api
 > livewire
    Would you like dark mode support? (yes/no) [no]
 > yes
   Which testing framework do you prefer? [PHPUnit]
        PHPUnit .............................................................................. 0
        Pest ................................................................................. 1
 > 0
 > git add .
    warning: in the working copy of 'package.json', CRLF will be replaced by LF the next time Git touches it
 > git commit -m "Instalação do Breeze (livewire)"

## Instalação Tailwind

    > npm install -D tailwindcss postcss autoprefixer
    > npx tailwindcss init -p
    > git add .
    > git commit -m "Instalação Tailwind" 

## > code

    Ativar VSCode

### Configurar Idioma/Timezone

        link
            https://github.com/lucascudo/laravel-pt-BR-localization
        > php artisan lang:publish
        > composer require lucascudo/laravel-pt-br-localization --dev
        > php artisan vendor:publish --tag=laravel-pt-br-localization
        Alterar \config\app.php para: (Linha 86 do arquivo )
            De > 'locale' => 'en',
            P/ > 'locale' => 'pt_BR'
        Alterar \config\app.php para: (Linha 73 do arquivo )
            De 'timezone' => 'UTC',
            P\ 'timezone' => 'America/Sao_Paulo',
        > git add .
        > git commit -m "Configurar Idioma/Timezone" 

### Apontar banco de dados no arquivo .env ( De laravel P/ db_sll)

        DB_CONNECTION=mysql
        DB_HOST=127.0.0.1
        DB_PORT=3306
        DB_DATABASE=db_sll
        DB_USERNAME=root
        DB_PASSWORD=

#### Criar tabela padrão no banco de dados ( users)

        > php artisan migrate:fresh

#### Descomentar database\seeders\DatabaseSeeder.php

        \App\Models\User::factory(10)->create();

#### Popular tabela users

        > php artisan db:seed

## Publicar GitHub

    > git remote add origin https://github.com/robertomrr/09_CLGVT_LW.git
    > git branch -M main
    > git push -u origin main

## Ativar Aplicação utilizando terminal CMD | Git Bash

    > CMD 
        > cd C:\laragon\www\sem-lero-lero
        > npm run dev
        > php artisan serve
    > Browser
        > localhost:8000

## Após clone recompor aplicação com os arquivos ignorados

    > composer update
    > npm install
    > copy .env.example .env
    > php artisan key:generate
