# VoIP-платформа с Kamailio, FreeSWITCH и RTPengine

## 📘 Описание

- **Kamailio** — в качестве SIP-сервера регистрации.
- **FreeSWITCH** — для обработки конференций.
- **RTPengine** — для обработки медиапотока
- **FreeSWITCH** — также может напрямую обрабатывать RTP-поток, в зависимости от конфигурации.


## 🧩 Архитектура

```plaintext
SIP UA1 <--> Kamailio <--> FreeSWITCH <--> SIP UA2
           |
           +--> RTPengine (вариант 1: медиапоток через RTPengine)
           |
           +--> FreeSWITCH (вариант 2: медиапоток через FreeSWITCH напрямую)
