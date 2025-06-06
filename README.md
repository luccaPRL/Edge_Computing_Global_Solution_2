# 🚨 Projeto de Monitoramento de Enchentes com Arduino

Este projeto tem como objetivo a criação de um sistema simples de alerta de enchentes utilizando sensores básicos como potenciômetro (nível de água), LDR (sensor de luz para simular chuva), buzzer e LED.

---

## 🎓 Integrantes do Grupo

- **Diego Garcia Tosta** — RM: 556724  
- **Joud Jihad Jaber** — RM: 556482  
- **Lucca Pereira** — RM: 560731

---

## ⚙️ Componentes Utilizados

- Arduino Uno  
- Potenciômetro (nível de água)  
- LDR (fotoresistor)  
- Resistor de 10kΩ (para LDR)  
- LED vermelho  
- Resistor de 220Ω (para LED)  
- Buzzer piezoelétrico  
- Jumpers (cabos de conexão)  
- Protoboard

---

## 🔌 Conexões dos Componentes

### 🔹 Potenciômetro (nível de água)
- VCC → 5V  
- GND → GND  
- Sinal → A0

### 🔹 LDR com Resistor de 10kΩ (chuva)
- Uma ponta do **LDR** → 5V  
- Outra ponta do **LDR** → A1 **e** uma ponta do resistor de 10kΩ  
- Outra ponta do **resistor** → GND

### 🔹 LED de alerta
- Perna longa do LED (ânodo) → Resistor 220Ω → Pino 13  
- Perna curta do LED (cátodo) → GND

### 🔹 Buzzer
- Positivo (+) → Pino 12  
- Negativo (–) → GND

---

## 🧠 Lógica do Código

O sistema monitora dois fatores:
- **Nível de água** (potenciômetro)
- **Chuva** (intensidade de luz captada pela LDR)

Se ambos os valores ultrapassarem os limites definidos:
- O **LED** acende como alerta visual
- O **Buzzer** emite um som como alerta sonoro
- Uma mensagem é exibida no **monitor serial**

---

## ✅ Observações

- O código foi desenvolvido em linguagem C/C++ para a IDE do Arduino.
- As leituras dos sensores são feitas com `analogRead()` nos pinos A0 e A1.
- O sistema funciona com um atraso de 2 segundos entre cada leitura (`delay(2000)`).
