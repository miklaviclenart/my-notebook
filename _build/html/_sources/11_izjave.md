# Izjave in izjavni vezniki

> Neformalna definicija
> : V klasični logiki z besedo _izjava_ označujemo pripovedno povéd, ki je bodisi resnična bodisi neresnična.

```{admonition} Zgled 1
* Poved "Ena in ena je dva." je resnična izjava.
* Poved "Dva je liho število." je neresnična izjava.
* Vprašalna poved "Ali je dva sodo število?" **ni** izjava.
* Velelna poved "Izračunaj vsoto prvih 100 naravnih števil!" **ni** izjava.
* Vzemimo poved "Ta povéd ni resnična". Če bi bila resnična, bi bilo res, kar trdi sama o sebi – torej bi bila neresnična; in če bi bila neresnična, bi bila laž,
kar trdi sama o sebi – torej bi bila resnična. Zato ta povéd ni izjava.
```

Izjave **po vsebini** delimo na:

1. _resnične_, ki jim pripišemo resničnostno vrednost 1,
2. _neresnične_, ki jim pripišemo resničnostno vrednost 0.

Namesto 1, 0 se uporabljata tudi simbola $\top$, $\bot$ (beri _vrh_,_dno_) ali _true_, _false_.

Izjave **po obliki** delimo na:

1. _osnovne_, ki ne vsebujejo izjavnih veznikov,
2. _sestavljene_, ki vsebujejo vsaj en izjavni veznik.

---
Preden definiramo izjavne veznike, si oglejmo nekaj zgledov.

```{admonition} Zgled 2
* Izjavi "Vreme je lepo" in "Peter gre v hribe" sta osnovni.
* Izjave

  * "Vreme je lepo in Peter gre v hribe",
  * "Če je vreme lepo, (potem) gre Peter v hribe",
  * "Peter ne gre v hribe"

  so sestavljene iz gornjih dveh osnovnih izjav s pomočjo izjavnih veznikov **in**, **če – potem** in **ne**.
```

V gornjem zgledu sta izjavna veznika 'in' ter 'če – potem' dvomestna, veznik 'ne' pa
je enomesten. V splošnem lahko z $n$-mestnim izjavnim veznikom, kjer je $n$ neko
naravno število, $n$ poljubnih izjav povežemo v novo izjavo.

Zahteva
: Resničnostna vrednost sestavljene izjave sme biti odvisna le od uporabljenega izjavnega veznika in od resničnostnih vrednosti izjav, ki jo sestavljajo.

To med drugim pomeni, da ni vsak slovnični veznik tudi izjavni veznik.

```{admonition} Zgled 3
Recimo, da je torek, da sije sonce in da je toplo. Potem so vsi sestavni
deli izjav “Ker sije sonce, je toplo” in “Ker je torek, je toplo” resnični, vendar je
prva morda resnična, druga pa najbrž ne. Veznik ker torej ni izjavni veznik, saj je
resničnost izjave, sestavljene z njegovo pomočjo, odvisna od tega, ali med njenima
sestavnima deloma obstaja vzročna zveza ali ne.
```

Po gornji zahtevi je resničnostna vrednost sestavljene izjave enolično določena
z resničnostnimi vrednostmi njenih sestavnih delov, zato lahko izjavni veznik definiramo kot neko preslikavo oziroma funkcijo:
> Definicija 1
> : Naj bo $n$ naravno število. Preslikavo, ki vsaki urejeni $n$-terici, sestavljeni iz ničel in enojk,
priredi vrednost 0 ali 1, imenujemo $n$-mestni izjavni veznik ali tudi _Boolova funkcija_ $n$ spremenljivk.

Definicijsko območje $n$-mestnega izjavnega veznika je torej množica vseh urejenih $n$-teric, sestavljenih iz ničel in enojk, ki ima $2^n$
elementov. Naštejmo nekaj
standardnih izjavnih veznikov:

* _enomestni_: negacija
* _dvomestni_: konjunkcija, disjunkcija, implikacija, ekvivalenca.

Kako zapišemo in kako preberemo dobljeno sestavljeno izjavo, kaže naslednja tabela. V njej sta $p$ in $q$ poljubni izjavi.

ime veznika |   simbolni zapis izjave   |   kako preberemo sestavljeno izjavo
:----------:|:-------------------------:|:-------------------------------------:
negacija    |   $\neg p$                |   ne $p$
konjunkcija |   $p \land q$             |   $p$ in $q$
disjunkcija |   $p \lor q$              |   $p$ ali $q$
implikacija |   $p \implies q$          |   iz $p$ sledi $q$
ekvivalenca |   $p \iff q$              |   $p$ natanko tedaj, ko $q$

Izjavo $p$ imenujemo _antecedens_, izjavo $q$ pa _konsekvens_ implikacije $p \implies q$.

Ker je definicijsko območje $n$-mestnega izjavnega veznika končna množica, ga lahko
podamo s tabelo resničnostnih vrednosti pri vseh $2^n$ možnih argumentih, ki jo
imenujemo _resničnostna tabela_ veznika. Resničnostne tabele negacije, konjunkcije,
disjunkcije, implikacije in ekvivalence so naslednje:

$p$  | $\neg p$
:---:|:--------:
1    |  0
0    |  1

$p, q$  |   $p \land q$ |   $p \lor q$  |   $p \implies q$  |   $p \iff q$
:------:|:-------------:|:-------------:|:-----------------:|:-------------:
1, 1    |   1           |   1           |   1               |   1
1, 0    |   0           |   1           |   0               |   0
0, 1    |   0           |   1           |   1               |   0
0, 0    |   0           |   0           |   1               |   1

Z besedami: Negacija spremeni resničnostno vrednost. Konjunkcija je resnična
natanko tedaj, ko sta resnična oba njena člena; disjunkcija, ko je resničen vsaj
eden od členov; implikacija, ko je resničen njen konsekvens ali ko je neresničen njen
antecedens; ekvivalenca pa, ko imata njena člena enako resničnostno vrednost.

Koristila nam bosta tudi ničmestna izjavna veznika 0 in 1, ki nič izjav "povežeta" v izjavni konstanti 0 oziroma 1.
Tu si izjavno konstanto 0 predstavljamo kot neko splošno neresnično izjavo,
izjavno konstanto 1 pa kot neko splošno resničnoizjavo.
Simbola 0 in 1 igrata torej trojno vlogo, saj lahko predstavljata

* resničnostni vrednosti,
* ničmestna izjavna veznika,
* izjavni konstanti;

za katero vlogo gre, v vsakem posameznem primeru razberemo iz sobesedila.

Vprašajmo se še: Koliko je vseh možnih $n$-mestnih izjavnih veznikov? Vsak tak
veznik podamo z njegovo resničnostno tabelo, ki vsebuje $2^n$ vrstic. Ker imamo v
vsaki vrstici za vrednost veznika dve možnosti (0 ali 1), je število vseh $n$-mestnih
izjavnih veznikov enako $2^{2^n}$, kar je izredno hitro rastoča funkcija argumenta $n$.
