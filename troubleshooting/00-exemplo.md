# Erro de push com histórico diferente

**Eu acabei de ter um problema assim:**  
> Fui tentar fazer um `git push` e o terminal me retornou `error: failed to push some refs`. Isso aconteceu porque alguém tinha subido código no repositório remoto e eu não tinha puxado antes.

**E a solução foi esse comando:**  
```bash
git pull origin main --rebase
git push origin main
```

**Ele serve para tal coisa:**  
> O `pull --rebase` baixa as alterações que estavam no GitHub e coloca os meus commits locais "por cima" deles. Isso evita aquele commit automático chato de merge e deixa a linha do tempo limpa. Depois disso, o `push` funciona normalmente.