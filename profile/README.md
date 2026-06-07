# Voylo: Voice AI Infrastructure for the AI Era

**Build voice experiences that actually pick up the phone.**

Voylo is the voice infrastructure that turns any AI provider into a phone service. One number, unlimited routing possibilities — failover between providers, IVR flows, rate limiting, real-time switching — all controlled by simple XML (VoyloML).

## 🚀 What We Do

**Problem:** Every AI voice provider has an API. None of them answer phone calls.

**Solution:** Voylo bridges SIP telephony to AI providers, so your ElevenLabs agent, Vapi assistant, or LiveKit room can have a real phone number in 150+ countries.

```
Phone Call → Your Number → Voylo Trunk → VoyloML App → Any AI Provider
```

## 📚 Quick Links

- **[Documentation](https://voylo.ai/docs)** — Complete API reference and guides
- **[Console](https://voylo.ai/app)** — Get your first number in 2 minutes
- **[Examples](#examples)** — Production-ready code you can deploy today

## 🛠 Examples

Our example repos demonstrate real patterns you'll need in production. Each runs out of the box.

### Getting Started
- **[voyloml-starter](https://github.com/voylo-labs/voyloml-starter)** — Hello world: answer a call and speak (5 min)

### Production Recipes
- **[voylo-elevenlabs-ivr-failover](https://github.com/voylo-labs/voylo-elevenlabs-ivr-failover)** — Protect your ElevenLabs quota with rate limiting, IVR menu, and automatic failover

### Provider Integrations
- **ElevenLabs** — Give your conversational AI a phone number
- **Vapi** — Route phone calls to your Vapi assistant
- **LiveKit** — Bridge PSTN calls into your LiveKit rooms
- **Pipecat** — Connect telephony to your Pipecat agents
- **Retell AI** — Enable phone calls for Retell agents
- **OpenAI Realtime** — Voice calls with GPT-4 Realtime API

### Advanced Patterns
- **Multi-provider failover** — Primary + backup providers with automatic switching
- **IVR with human handoff** — Press 0 for a human, with context preservation
- **Rate limiting & abuse protection** — Per-caller quotas to prevent bill shock
- **Regional routing** — Route by caller location or number prefix
- **Call recording & webhooks** — Capture, transcribe, and process conversations

## 🔑 Core Concepts

**Number** — A phone number in any country (US, UK, UAE, etc.)
**Trunk** — Routes calls from your number to a VoyloML application
**VoyloML** — XML that controls the call flow (IVR, routing, failover)

That's it. Number → Trunk → VoyloML. Every example follows this pattern.

## 🏗 Architecture

```
┌─────────────┐     ┌─────────────┐     ┌──────────────┐     ┌────────────┐
│  Phone Call │────▶│ Your Number │────▶│ Voylo Trunk  │────▶│  VoyloML   │
└─────────────┘     └─────────────┘     └──────────────┘     └────────────┘
                                                                     │
                                              ┌──────────────────────┴───────────┐
                                              ▼                                  ▼
                                     ┌──────────────┐                   ┌──────────────┐
                                     │  ElevenLabs  │                   │     Vapi     │
                                     └──────────────┘                   └──────────────┘
                                              ▲                                  ▲
                                              └────────── Failover ──────────────┘
```

## 🚦 Getting Started

1. **Get a number** at [voylo.ai/app](https://voylo.ai/app) (2 min)
2. **Clone a starter**:
   ```bash
   git clone https://github.com/voylo-labs/voyloml-starter
   cd voyloml-starter
   ```
3. **Deploy** `app.xml` (GitHub Pages, Vercel, or any static host)
4. **Point your application** at your deployed URL
5. **Call your number** — it works

## 📜 License

All example code is MIT licensed. Use it, fork it, ship it.

---

**Building with Voylo?** We'd love to feature your use case. Tag [@VoyloAi](https://twitter.com/VoyloAi) and show us what you built.
