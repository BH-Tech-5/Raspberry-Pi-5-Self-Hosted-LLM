# Raspberry-Pi-5-Self-Hosted-LLM
**Overview:**
Privacy focused artificial intelligence utilizing Raspberry Pi 5, open source AI models, Tailscale, and OpenWebUI accessed via a Progressive Web Application.

**Instructions for Use:**
Utilizing the same technical stack,
1. Download and enable tailscale on your Pi and the accessing device.
2. Download ollama and pull whichever model works for your hardware.
3. Download docker onto your Pi.
4. Download OpenWebUI on the Pi and then access it via your accessing device's browser.

**Narrative:**
This was a much quicker project than the security camera as it only required downloading open source models to my Pi using curl commands, downloading OpenWebUI/Docker, and configuring access to it with a Progressive Web Application (PWA) on my phone.

One of the largest hurdles was realizing that larger models required further optimization

**Technical Stack:**
- Hardware: Raspberry Pi 5 8GB RAM
- Networking: Tailscale (WireGuard based) for encrypted end-to-end access.
- Presentation/Access: OpenWebUI, PWA on iPhone utilizing Safari

**Key Takeaways:**
- Privacy: No longer sharing data for harvesting and targeting.
- Autonomy: No longer relying on API key limits - I can query as many times as I like from anywhere.
- Optimization: Gained experience in deploying different models with different parameter counts.

**Evolution/Versions**
- The first iteration I conducted was using Llama3.2:3b. This model took up a significant amount of RAM while running and I realized that if I wanted search capabilities as well, I would need less of the overhead/CPU taken up by reasoning.
- I moved to Gemma2:2b in order to create more space for compute in searching.

**Future Developments:**
- Ability to search the web utilizing the local AI.
- Token-per-second optimization with quantized models due to limited compute.
