# __Git_study__ 
ππππππππππ

### __Git μ΄λ?__
- λ²μ μ νΈλ¦¬νκ² κ΄λ¦¬ν  μ μλλ‘ λμμ£Όλ λκ΅¬
- μμνκ³  μλ νμΌλ€μ μνλ μκ°μΌλ‘ λ€μ λμκ° μ μκ²λ λ§λ€μ΄μ£Όλ λκ΅¬
- VCS ( Version Control System )
- Distributed Version Control : λͺ¨λ  κ°λ°μλ€μ΄ λμΌν νμ€ν λ¦¬ μ λ³΄λ₯Ό κ°μ§κ³  μλ κ² ( λΆμ° μμ€ν )
- Snapshot νμμΌλ‘ μ μ₯λλ€. :camera:

### __Git μ μ₯μ __
1. most commonly used : λ³΄νΈμ μΌλ‘ μ¬μ©λκ³  μμ
2. free : λ¬΄λ£
3. open source : μ€νμμ€
4. lightning fast : λͺ¨λ  λμλ€μ΄ κ΅μ₯ν λΉ λ¦
5. work offline : μ€νλΌμΈμμλ μΌμ ν  μ μμ
6. undo mistakes : μ€μλ₯Ό λ€μ κ³ μ³λκ°κΈ°κ° μ¬μ
7. easy and fast branching/merging : μ½κ³  λΉ λ₯Έ λΈλμΉ­μ μ΄μ©ν΄μ κ°κ°μ λΈλμΉλ‘ ν¨μ¨μ μΈ νμ κ°λ₯

---
### __git config__
Gitμ μ€μΉνκ²λλ©΄ Gitμ κ΄λ ¨λ λͺ¨λ  νκ²½μ€μ μ΄ .gitconfig λΌλ νμΌ μμ μ μ₯μ΄ λλλ° ν°λ―Έλμμ νμΈν΄ λ³Ό μ μλ€.
- git config --list : λͺ¨λ  μ€μ  νμΈ κ°λ₯
- git config --global -e : μμ νκ³  μΆμ λ
- git config --global core.editor "code --wait" : configμμ μ vscodeλ‘ λ³κ²½
  - vscodeμμ Shell Command: Install 'code' ~ μ€μΉν΄μΌλ¨.
- git config --global user.name "~~~" : μ¬μ©μ μ΄λ¦ μ€μ 
- git config --global user.email "~~~" : μ¬μ©μ μ΄λ©μΌ μ€μ 
- git config user.name : μ¬μ©μ μ΄λ¦ μΆλ ₯
- git config --global core.autocrlf input/true : Mac:input, Window:true
  - μ΄μμ²΄μ λ§λ€ μλν°μμ μ€λ°κΏμ ν  λ λ€μ΄κ°λ λ¬Έμμ΄μ΄ λ¬λΌμ§. μ΄ λΆλΆμ λ§μΆ°μ£ΌκΈ° μν΄ μ€μ ν΄μ€μΌ ν¨!(carriage-return)
- git config -h : λͺλ Ήμ΄μμ μΈ μ μλ μμ±κ°λ€ μΆλ ₯

---

### __git init__
Git μ μ΄κΈ°ν μν€λ λͺλ Ήμ΄ : .git μμ± 

---
### __git status__
Git μ μνλ₯Ό λ³Ό μ μλ λͺλ Ήμ΄
  - git config --global alias.st status : git status -> git st 
  - git status -h : μΆκ°μ μΈ μμ±λ€ νμΈ κ°λ₯
  - default κ° : --long
  - git status -s : κ°λ¨ver

---
### __Git System κ°λ¨νκ² κ·Έλ €λ΄€μ΄μ__
<img src="./screenshot.png" width="500" height="280">

- Staging Area λ₯Ό commit λ€μ λ΄λ Box λΌκ³  μ΄ν΄νμ!
- Staging Area == stage
- λΆμ‘±νμ§λ§ μ΄ κ΅¬μ‘°μμ μμ μ κ±°μ³κ°λ©° κ³΅λΆν  μμ !^^

---
### __git add__
νμΌμ stageμ μ¬λ¦¬λ λͺλ Ήμ΄
  - modified : μμ λ νμΌ
  - git add . : ".gitignore"νμΌμ μλ νμΌλͺλ€μ μ μΈνκ³  stageμ μ¬λ¦¬λ λͺλ Ήμ΄
  - git add *  : ".gitignore"νμΌμ μλ νμΌλ€λ stageλ‘ μ¬λ¦¬λ λͺλ Ήμ΄

---
### __git rm --cached <fileμ΄λ¦>__
stageμ μ¬λ¦° νμΌμ λ€μ untracked μνλ‘ λλλ¦¬λ λͺλ Ήμ΄
  - μ¦ git μ μ¬λ¦¬μ§ μκ³  λ΄ local PCμλ§ λ¨κΈ°κ² λ€λ λ»

---
### __.gitigore__
echo λ¬΄μν΄μΌν νμΌ > .gitignore
  - "."μ΄ μμ λΆλ νμΌλ€μ μ¨κΉνμΌ
  - ex) log.log , \*.log , build/ , build\/*.log

---
### __git diff__
μ ννκ² μ΄λ€ λ΄μ©μ΄ μμ λμλμ§ νμΈνκΈ° μν λͺλ Ήμ΄
- git diff : working directory μμ μλ λ³κ²½μ¬ν­λ§ νμΈκ°λ₯
- git diff --staged : stageμ μλ λ³κ²½μ¬ν­ νμΈκ°λ₯
- git diff --cached : --staged λ λκ°μ
- vscode λ‘ λ³κ²½μ¬ν­ νμΈ κ°λ₯
  - git config --global -e λͺ¨λλ‘ μ΄μ΄μ νλ¨ μ½λ μλ ₯
    ```
    [diff]
      tool = vscode
    [difftool "vscode"]
      cmd = code --wait --diff $LOCAL $REMOTE
    ```
- git difftool (--staged) : vscodeλ‘ λ³κ²½μ¬ν­ νμΈκ°λ₯

---

### __git commit__
stageμ μλ λ³κ²½μ¬ν­μ Git repositoryμ μ?κ²¨μ£Όλ μ­ν 
- git commit -m "~~~" : μ»€λ°λ©μμ§ λ±λ‘
- git commit -am "~~~" : working directoryμ μλ λͺ¨λ  νμΌλ€μ λ©μμ§μ ν¨κ» commit

