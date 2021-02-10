# How to install elixir on Ubuntu?

## 1º Step

Go to oficial web site of elixir,
<a href="https://elixir-lang.org/install.html">Elixir Install</a>,
and select the operating system, in my case I'm using ubuntu 20.04.

## 2º Step (Ubuntu - Debian) 🐧

Add erlang repo

    apt-get install erlang

## 3º Step

Update your repo using:

    sudo apt-get update

## 4º Step

Install Erlang/OTP plataform apps

    sudo apt-get install esl-erlang

## 5º Step

Install Elixir

    sudo apt-get install elixir

<br>

# Using Windows 🏠

Download instaler <a href="https://github.com/elixir-lang/elixir-windows-setup/releases/download/v2.1/elixir-websetup.exe">here</a>,
and click in next, next, ...finish

## Using Chocolatey

    cinst elixir

<br>

# macOS 🍎

## Brew

Update your homebrew to latest

    brew update

and run:

    brew install elixir

## Macports

    sudo port install elixir
