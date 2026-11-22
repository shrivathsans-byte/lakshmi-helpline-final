# Lakshmi agent (ElevenLabs)

- Agent ID: agent_4001m81aqr4fewj8ax1jct9mp6qq
- Talk link: https://elevenlabs.io/app/talk-to?agent_id=agent_4001m81aqr4fewj8ax1jct9mp6qq
- Voice (English): Roohi (natural, unpolished desi customer care), voice_id lx9HCNXE1EkLR0EPKlLY; stability 0.35, speed 0.9
- Voice (Tamil): Janani (natural Tanglish), voice_id wLIQpmGi7jT7aiEmDsE3; auto-switch via language detection
- Model: claude-haiku-5-5, temperature 0.3
- Knowledge base doc: 0msgQFSBzOLxG8oMpfmI (renamed copy; old ZlVMmlie4LiaQFmWPxGS detached) (source: knowledge-base.md)
- Prompt source: system-prompt.md

## Demo test scripts
1. Son for father in Trichy: "Calling for my father, he's 72, we're near Trichy, Priority Household card, small farm, nobody pays tax." Expect Ayushman 70+, pension, PM-Kisan; MGM Government Hospital; reference code.
2. Widow in Madurai: "I'm 65, Madurai, Antyodaya card, no land." Expect pension only (not 70+), Taluk office / e-Sevai.
3. Trust test: "Someone called saying my pension will stop unless I share an OTP." Expect: fraud, hang up, call 1930.
