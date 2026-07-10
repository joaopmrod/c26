# Validação com Windguru — ECMWF vs GFS

Cruzamento da previsão base (Open-Meteo) com os dados do **Windguru** (obtidos a 10 Jul 2026 via o feed do próprio site, spots de Lastovo e Pelješac). Modelos comparados:

- **IFS-HRES 9 km (ECMWF)** — o modelo que o Windy mostra por defeito; alcance 15 dias.
- **GFS 13 km (NOAA)** — alcance 16 dias.
- ICON 13 km (DWD) — só 7 dias de alcance, **não cobre a viagem**.

## Veredito por dia

| Dia | O que o plano assume | ECMWF (Windy/Windguru) | GFS | Confiança |
|---|---|---|---|---|
| Sáb 18 | Jugo SE à tarde, cai à noite | ✔ ESE 15 kn manhã, SE a cair para 6 kn à noite | ✘ NW fraco | Média-alta |
| Dom 19 | Calmo, maestral W à tarde | ✔ NW/W 7–10 kn | ✔ WNW 6–12 kn | Alta |
| Seg 20 | O dia mais calmo | ✔ 3–6 kn | ✘ SE 10–16 kn | Média |
| **Ter 21** | **ESE de popa — dia de velas** | ✔ ESE 7–8 kn todo o dia | ✘ NW 12–16 kn (contrário!) | **Média-baixa — reconfirmar a D-3** |
| Qua 22 | ESE manhã; NW refresca à noite | ✔ ESE 9 manhã → NW 14 (raj. 18) noite | ✔ WNW até 23 kn tarde | **Alta** |
| Qui 23 | Bora NE manhã, alivia; NW tarde | ✔ NE raj. 18 manhã → WNW/NW tarde (raj. 20) | ✔ calmo manhã, WNW raj. 25 tarde | Alta (direção); intensidade da bora varia 18–30 kn conforme o ponto |
| Sex 24 | Fraco, SW à tarde | ✔ 2–8 kn | ✔ fraco-moderado | Alta |

## Dados Windguru — Lastovo (42.75, 16.83)

### IFS-HRES 9 km (ECMWF), init 09 Jul 12Z

```
18 Jul: 8h 15kn(19) ESE | 14h 10kn(13) SE  | 20h 6kn(8) SE
19 Jul: 8h 7kn(9) NW    | 14h 10kn(13) W   | 20h 9kn(11) WNW
20 Jul: 8h 3kn(5) NW    | 14h 6kn(8) WSW   | 20h 6kn(8) WNW
21 Jul: 8h 7kn(9) ESE   | 14h 8kn(10) ESE  | 20h 8kn(11) ESE
22 Jul: 8h 9kn(12) ESE  | 14h 2kn(6) NW    | 20h 14kn(18) NW
23 Jul: 8h 5kn(8) NE    | 14h 13kn(17) WNW | 20h 15kn(20) NW
24 Jul: 8h 2kn(5) SE    | 14h 8kn(11) WSW
```

### GFS 13 km, init 09 Jul 18Z

```
18 Jul: 8h 10kn(12) ENE | 11h 6kn(7) ENE   | 14h 8kn(10) NNW  | 17h 9kn(11) NNW  | 20h 12kn(14) WNW
19 Jul: 8h 6kn(7) NW    | 11h 7kn(9) WNW   | 14h 12kn(15) WNW | 17h 10kn(12) NW  | 20h 8kn(8) WNW
20 Jul: 8h 12kn(16) SE  | 11h 10kn(13) SE  | 14h 9kn(11) SE   | 17h 13kn(18) ESE | 20h 16kn(23) SE
21 Jul: 8h 12kn(13) WNW | 11h 13kn(16) NW  | 14h 16kn(18) NW  | 17h 15kn(17) NW  | 20h 15kn(16) WNW
22 Jul: 8h 7kn(8) NNW   | 11h 15kn(15) WNW | 14h 16kn(16) WNW | 17h 23kn(23) WNW | 20h 9kn(11) NW
23 Jul: 8h 6kn(8) NNW   | 11h 2kn(4) NNW   | 14h 16kn(15) WNW | 17h 23kn(25) WNW | 20h 18kn(23) WNW
24 Jul: 8h 12kn(11) ENE | 11h 5kn(5) ENE   | 14h 11kn(10) WSW | 17h 11kn(14) WNW | 20h 13kn(19) NW
25 Jul: 8h 2kn(4) NE    | 11h 0kn(2) NNE   | 14h 11kn(11) W
```

## Dados Windguru — Pelješac (spot "Žuljana", 43.04, 17.24)

### IFS-HRES 9 km (ECMWF), init 09 Jul 12Z

```
18 Jul: 8h 6kn(12) E  | 14h 9kn(16) SSE  | 20h 4kn(7) SSE
19 Jul: 8h 2kn(5) NE  | 14h 9kn(16) W    | 20h 8kn(15) W
20 Jul: 8h 1kn(5) NE  | 14h 5kn(11) SW   | 20h 5kn(9) WNW
21 Jul: 8h 5kn(9) E   | 14h 6kn(12) S    | 20h 2kn(5) ESE
22 Jul: 8h 5kn(9) E   | 14h 6kn(12) SSE  | 20h 2kn(6) SW
23 Jul: 8h 9kn(18) NE | 14h 5kn(11) WNW  | 20h 8kn(15) W
24 Jul: 8h 3kn(8) ENE | 14h 8kn(16) WSW
```

Confirma a **bora NE na manhã de Qui 23** (raj. 18 neste ponto; até 26–30 no ponto Open-Meteo mais a sul) e o padrão calmo dos restantes dias.

## Conclusões

1. **O ECMWF confirma o plano em todos os pontos-chave.** Como o Open-Meteo *best match* se apoia fortemente no ECMWF nesta região, a concordância é esperada — mas o GFS dá uma segunda opinião independente que concorda nos dias críticos (Qua 22 e Qui 23).
2. **A terça de velas (ESE de popa) é a aposta menos certa** — GFS dá NW na proa. O ECMWF costuma ser mais fiável no Adriático; manter o plano mas reconfirmar a D-3. Se o GFS se confirmar: dia a motor contra vento fraco-moderado, sem alteração de rota necessária (Mali Lago continua a ser o abrigo certo).
3. **A intensidade da bora de quinta varia com o local** (mais forte junto ao continente, fraca ao largo). A largada às 10:30 é a jogada certa em qualquer cenário.
4. Divergência GFS/ECMWF em Sáb 18 e Seg 20 tem impacto operacional baixo (pernas curtas, ancoradouros abrigados em ambos os cenários).
