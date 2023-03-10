# 10) Git workflow κ°λ

---

<aside>
π‘ **Branchλ₯Ό μ΄μ©ν΄ νμμ νλ λ κ°μ§ λ°©λ²**μ λν΄ μμλ΄λλ€.
1. μκ²© μ μ₯μ μμ κΆμ΄ μλ κ²½μ° (Shared repository model)
2. μκ²© μ μ₯μ μμ κΆμ΄ μλ κ²½μ° (Fork & Pull model)

</aside>

## [1] μκ²© μ μ₯μ μμ κΆμ΄ μλ κ²½μ° (Shared repository model)

### (1) κ°λ

- μκ²© μ μ₯μκ° μμ μ μμ μ΄κ±°λ collaboratorλ‘ λ±λ‘λμ΄ μλ κ²½μ°μ κ°λ₯ν©λλ€.
- masterμ μ§μ  κ°λ°νλ κ²μ΄ μλλΌ, `κΈ°λ₯λ³λ‘ λΈλμΉ`λ₯Ό λ°λ‘ λ§λ€μ΄μ κ°λ°ν©λλ€.
- `Pull Request`λ₯Ό κ°μ΄ μ¬μ©νμ¬ νμ κ° λ³κ²½ λ΄μ©μ λν μν΅μ μ§νν©λλ€.

### (2) μμ νλ¦

1. μμ κΆμ΄ μλ μκ²© μ μ₯μλ₯Ό λ‘μ»¬ μ μ₯μλ‘ `clone` λ°μ΅λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9d8aab56-c8b0-4d72-9bb9-0cb1789761ae/Untitled.png)
    
    ```bash
    $ git clone https://github.com/edukyle/django-project.git
    ```
    

1. μ¬μ©μλ μμ μ΄ μμν  κΈ°λ₯μ λν `λΈλμΉλ₯Ό μμ±`νκ³ , κ·Έ μμμ `κΈ°λ₯μ κ΅¬ν`ν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d6ec3f5c-abb0-44be-b923-c57373606795/Untitled.png)
    
    ```bash
    $ git switch -c feature/login
    ```
    

1. κΈ°λ₯ κ΅¬νμ΄ μλ£λλ©΄, μκ²© μ μ₯μμ ν΄λΉ λΈλμΉλ₯Ό `push` ν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/90c5722c-9ac9-4c60-a250-421a313222cb/Untitled.png)
    
    ```bash
    $ git push origin feature/login
    ```
    

1. μκ²© μ μ₯μμλ masterμ κ° κΈ°λ₯μ λΈλμΉκ° λ°μλμμ΅λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9c8e693a-241f-41f6-88d4-ef127c7c4b14/Untitled.png)
    

1. Pull Requestλ₯Ό ν΅ν΄ λΈλμΉλ₯Ό masterμ λ°μν΄λ¬λΌλ μμ²­μ λ³΄λλλ€.
(νμλ€κ³Ό μ½λ λ¦¬λ·°λ₯Ό ν΅ν΄ μν΅ν  μ μμ΅λλ€.)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2ced8346-37e0-4291-8811-fe0d2422539d/Untitled.png)
    
2. λ³ν©μ΄ μλ£λλ©΄ μκ²© μ μ₯μμμ λ³ν©μ΄ μλ£λ λΈλμΉλ λΆνμνλ―λ‘ μ­μ ν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eb9c4d7e-ebd9-4016-8306-3882ad791464/Untitled.png)
    

1. masterμ λΈλμΉκ° λ³ν©λλ©΄, κ° μ¬μ©μλ λ‘μ»¬μ master λΈλμΉλ‘ μ΄λν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f95c707b-3ad3-41c3-beee-00eba8db2789/Untitled.png)
    
    ```bash
    $ git switch master
    ```
    

1. λ³ν©μΌλ‘ μΈν΄ λ³κ²½λ μκ²© μ μ₯μμ master λ΄μ©μ λ‘μ»¬μ λ°μμ΅λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/139021e6-2d00-4099-8205-2dca5e35f445/Untitled.png)
    
    ```bash
    $ git pull origin master
    ```
    

1. λ³ν©μ΄ μλ£λ masterμ λ΄μ©μ λ°μμΌλ―λ‘, κΈ°μ‘΄ λ‘μ»¬ λΈλμΉλ μ­μ ν©λλ€. (ν μ¬μ΄ν΄ μ’λ£)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cc543835-9e05-4f4f-a6d5-acc96f6ba91f/Untitled.png)
    
    ```bash
    $ git branch -d feature/login
    ```
    

1. μλ‘μ΄ κΈ°λ₯ μΆκ°λ₯Ό μν΄ μλ‘μ΄ λΈλμΉλ₯Ό μμ±νλ©° μ κ³Όμ μ λ°λ³΅ν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c96da544-1374-4921-b4dc-417a890adcf2/Untitled.png)
    
    ```bash
    $ git switch -c feature/pay
    ```
    

## [2] μκ²© μ μ₯μ μμ κΆμ΄ μλ κ²½μ° (Fork & Pull model)

### (1) κ°λ

- μ€ν μμ€ νλ‘μ νΈμ κ°μ΄, μμ μ μμ κ° μλ μκ²© μ μ₯μμΈ κ²½μ° μ¬μ©ν©λλ€.
- μλ³Έ μκ²© μ μ₯μλ₯Ό κ·Έλλ‘ λ΄ μκ²© μ μ₯μμ `λ³΅μ `ν©λλ€. (μ΄ νμλ₯Ό `fork`λΌκ³  ν©λλ€.)
- κΈ°λ₯ μμ± ν `Pushλ λ³΅μ ν λ΄ μκ²© μ μ₯μμ μ§ν`ν©λλ€.
- μ΄ν `Pull Request`λ₯Ό ν΅ν΄ μλ³Έ μκ²© μ μ₯μμ λ°μλ  μ μλλ‘ μμ²­ν©λλ€.

### (2) μμ νλ¦

1. μμ κΆμ΄ μλ μκ²© μ μ₯μλ₯Ό `fork`λ₯Ό ν΅ν΄ λ΄ μκ²© μ μ₯μλ‘ `λ³΅μ `ν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e1c48127-e989-4fd5-b697-aecf54cd21e0/Untitled.png)
    
    μλμ κ°μ΄ `Fork` λ²νΌμ λλ₯΄λ©΄ μλμΌλ‘ λ΄ μκ²© μ μ₯μμ λ³΅μ λ©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c3c3ff28-9a8d-4429-ad78-740a059e6457/Untitled.png)
    

1. `fork` ν, λ³΅μ λ λ΄ μκ²© μ μ₯μλ₯Ό λ‘μ»¬ μ μ₯μμ `clone` λ°μ΅λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e8628903-8781-41fe-a034-6e9746eb5407/Untitled.png)
    
    ```bash
    $ git clone https://github.com/edukyle/kakao_clone.git
    ```
    

1. μ΄νμ λ‘μ»¬ μ μ₯μμ μλ³Έ μκ²© μ μ₯μλ₯Ό λκΈ°ν νκΈ° μν΄μ μ°κ²°ν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0bbcb751-e5c2-49b6-8eb5-f6bc71c39aa8/Untitled.png)
    
    ```bash
    # μλ³Έ μκ²© μ μ₯μμ λν μ΄λ¦μ upstreamμΌλ‘ λΆμ΄λ κ²μ΄ μΌμ’μ κ΄λ‘
    
    $ git remote add upstream https://github.com/AlexKwonPro/kakao_clone.git
    ```
    

1. μ¬μ©μλ μμ μ΄ μμν  κΈ°λ₯μ λν `λΈλμΉλ₯Ό μμ±`νκ³ , κ·Έ μμμ `κΈ°λ₯μ κ΅¬ν`ν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0d535639-8145-430c-aebd-eee2fb8d5bbb/Untitled.png)
    
    ```bash
    $ git switch -c feature/login
    ```
    
2. κΈ°λ₯ κ΅¬νμ΄ μλ£λλ©΄, `λ³΅μ  μκ²© μ μ₯μ(origin)`μ ν΄λΉ λΈλμΉλ₯Ό `push` ν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0cc34aa6-0689-47c6-a71a-0f36de47eb28/Untitled.png)
    
    ```bash
    $ git push origin feature/login
    ```
    
3. `λ³΅μ  μκ²© μ μ₯μ(origin)`μλ masterμ λΈλμΉκ° λ°μλμμ΅λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ed7ed6b1-894c-4c40-862d-c84eb2431112/Untitled.png)
    

1. `Pull Request`λ₯Ό ν΅ν΄ `λ³΅μ  μκ²© μ μ₯μ(origin)μ λΈλμΉ`λ₯Ό `μλ³Έ μκ²© μ μ₯μ(upstream)μ master`μ λ°μν΄λ¬λΌλ μμ²­μ λ³΄λλλ€. 
(μλ³Έ μκ²© μ μ₯μμ κ΄λ¦¬μκ° μ½λ λ¦¬λ·°λ₯Ό μ§ννμ¬ λ°μ μ¬λΆλ₯Ό κ²°μ ν©λλ€.)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c82e4c12-dc9a-48f3-bba9-f9dca06eb5a1/Untitled.png)
    

1. `μλ³Έ μκ²© μ μ₯μ(upstream)`μ masterμ λΈλμΉκ° λ³ν©λλ©΄ `λ³΅μ  μκ²© μ μ₯μ(origin)`μ λΈλμΉλ μ­μ ν©λλ€. κ·Έλ¦¬κ³  μ¬μ©μλ λ‘μ»¬μμ master λΈλμΉλ‘ μ΄λν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/88eabf2b-490c-4e22-b284-8c3789b1729e/Untitled.png)
    
    ```bash
    $ git switch master
    ```
    

1. λ³ν©μΌλ‘ μΈν΄ λ³κ²½λ `μλ³Έ μκ²© μ μ₯μ(upstream)μ master` λ΄μ©μ λ‘μ»¬μ λ°μμ΅λλ€. 
κ·Έλ¦¬κ³  κΈ°μ‘΄ λ‘μ»¬ λΈλμΉλ μ­μ ν©λλ€. (ν μ¬μ΄ν΄ μ’λ£)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a213ba54-b4c1-487a-9745-f6316928f3bd/Untitled.png)
    
    ```bash
    $ git pull upstream master
    $ git branch -d feature/login
    ```
    

1. μλ‘μ΄ κΈ°λ₯ μΆκ°λ₯Ό μν΄ μλ‘μ΄ λΈλμΉλ₯Ό μμ±νλ©° μ κ³Όμ μ λ°λ³΅ν©λλ€.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d9e93191-e93c-4395-baaf-127d88cdf729/Untitled.png)
    
    ```bash
    $ git switch -c feature/pay
    ```