+++
title = "Computer setup (en)"
+++

संस्कृतेन सूचना द्रष्टुम् [अत्र गम्यताम्](../computer-setup_sa/) ।

## Common setup
- Below, replace XYZ with your github username.
- If https://github.com/XYZ/kalpAntaram exists beforehand, please delete it by going to settings using your browser.
- Go to https://github.com/vishvAsa/kalpAntaram and fork (there should be a Fork button in the top-right). Thence, you will get https://github.com/XYZ/kalpAntaram . 

## Going to the right place in your computer
- We'll assume that you're saving all github files in some location such as the ones used below.
- Please open terminal/ command-prompt in your computer.
  - In Windows, do something like: `cd F:\Git\`
  - In linux, do something like: `cd ~` .

## Getting the files
- Having followed "Going to the right place in your computer", doe the below

```
git clone --single-branch --depth 1 --branch master https://github.com/XYZ/kalpAntaram.git kalpAntaram-master
cd kalpAntaram-master
git remote add upstream https://github.com/vishvAsa/kalpAntaram.git
git submodule update --init  themes/sanskrit-documentation-theme-hugo
cd ..

git clone --single-branch --depth 1 --branch content https://github.com/XYZ/kalpAntaram.git kalpAntaram-content
cd kalpAntaram-content
git remote add upstream https://github.com/vishvAsa/kalpAntaram.git
git pull upstream content
cd ..

git clone --single-branch --depth 1 --branch static_files https://github.com/XYZ/kalpAntaram.git kalpAntaram-static
cd kalpAntaram-static
git remote add upstream https://github.com/vishvAsa/kalpAntaram.git
git pull upstream static_files
cd ..
```

## Running hugo
- Having followed "Going to the right place in your computer", and having retrieved the files as described above, 
- do the below to run `hugo` to build the website on your computer (so that you can verify that everything appears as it should).

```
cd kalpAntaram-master
git pull upstream master
cd themes/sanskrit-documentation-theme-hugo/
git pull origin master
cd ../.. 
hugo server --renderToDisk --config ./config_dev.toml
```

## Submitting file changes
- If you're chaning files in `kalpAntaram-content` :
    - Make sure that you're working on the latest files by running: `git pull upstream content` .
    - Then, commit and push your changes (using atom editor, or github desktop or commands like `git commit -am "Some message"` and `git push`).
    - Then go to https://github.com/XYZ/kalpAntaram/tree/content and send a pull request .
- If you're changing files in `kalpAntaram-static` :
  - Make sure that you're working on the latest files by running: `git pull upstream static_files` .
  - Then, commit and push your changes (using atom editor, or github desktop or commands like `git commit -am "Some message"` and `git push`).
  - Then go to https://github.com/XYZ/kalpAntaram/tree/static_files and send a pull request .
