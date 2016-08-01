# atframework starter

Windows
---

see https://jekyllrb.com/docs/windows/#installation

```
@powershell -NoProfile -ExecutionPolicy unrestricted -Command "(iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))) >$null 2>&1" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin

chcp 65001

choco install ruby ruby2.devkit -y

cd C:\tools\DevKit2
ruby dk.rb init
```

Then edit C:\tools\DevKit2\config.yml to add ruby root into it. And then:

```
ruby dk.rb install
```

Add more source.

```
cinst -Source "https://go.microsoft.com/fwlink/?LinkID=230477" libxml2

cinst -Source "https://go.microsoft.com/fwlink/?LinkID=230477" libxslt

cinst -Source "https://go.microsoft.com/fwlink/?LinkID=230477" libiconv
``` 

Change ruby mirror:

```
gem sources --add https://ruby.taobao.org/ --remove https://rubygems.org/
gem sources -l
gem install bundler
bundle config mirror.https://rubygems.org https://ruby.taobao.org
```

Or using ruby-china
```
gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/
gem sources -l
gem install bundler
bundle config mirror.https://rubygems.org https://gems.ruby-china.org
```

Or change Gemfile **source 'https://rubygems.org/'** into **source 'https://gems.ruby-china.org/'** or **source 'https://ruby.taobao.org/'**

At last, install jekyll
```
gem install jekyll
cd [website root]
bundle install
```

Other platforms
------


Just install ruby using yum or dnf or apt or pacman or brew or other tools.

Change ruby mirror just like in Windows.

Last, install jekyll
```bash
gem install jekyll ;
cd [website root] ;
bundle install ;
```

Plugins
------

```bash
cd [website root]

gem install jekyll-multiple-languages

gem install jekyll-paginate

gem install redcarpet
```