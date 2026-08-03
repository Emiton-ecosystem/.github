# Emiton

**IPTV/OTT platform that runs on one server.**

Headend, transcoding, statistical multiplexing, playout and delivery — a single
box instead of a rack. Built by broadcast engineers who run it in production.

**[Website](https://emiton.eu)** · **[Statmux](https://emiton.eu/statmux/)** · **[Docs](https://transcoder.sk/help)** · **[Demo](https://transcoder.sk/demo)** · **[Pricing](https://emiton.eu/pricing/)**

---

## What it does

| Module | |
|---|---|
| **Transcoding** | NVENC/NVDEC hardware pipeline. 30+ channels per node on a pair of RTX 5070 Ti. |
| **Statmux** | Software statistical multiplexer with per-frame complexity analysis on CUDA. |
| **Playout** | Scheduled playout, loop channels, ad insertion, deterministic XMLTV EPG. |
| **Delivery** | MPEG-TS multicast, HLS, DASH, SRT, RIST. DVB-C/DVB-T output for cable headends. |
| **Client apps** | White-label RUBIKON apps for Samsung Tizen, LG webOS, Android TV, mobile, STB and web. |
| **Billing** | Metron — CRM, invoicing and subscriber management. |

## Running in production

Emiton is not a reference design. It carries the live DVB-C and IPTV service of
[OSTV](https://ostv.sk) (AS209531), a Slovak cable and internet operator:

**7 transponders** at 256-QAM · **107 services** · DVB-C and OTT delivered in parallel from the same headend.

## Statmux, measured

Statistical multiplexing is usually a hardware purchase. Emiton does it in
software, and the numbers hold up against a CBR baseline on the same transponder
at identical mux bitrate:

- **98.4%** transport stream fill — 37.99 Mbps of 38.61 Mbps capacity
- **+3.98 VMAF** on the worst-case channel versus constant bitrate
- No dedicated multiplexer hardware

Methodology and full measurement data: **[statmux page](https://emiton.eu/statmux/)**

## Who it's for

Cable operators, IPTV providers and regional broadcasters who need a headend
that fits their scale — not a carrier-grade cluster with a carrier-grade price.

If you are running a DVB-C or DVB-T headend and looking at a six-figure quote
for a statmux, start with the measurements above.

---

## This organization

The Emiton platform is commercial and closed-source. This organization holds the
open surface around it — the parts you would otherwise have to reverse-engineer
to integrate with us:

- API specifications and client libraries
- EPG and XMLTV tooling
- TSDuck-based diagnostic scripts
- Prometheus exporters and monitoring integrations
- Deployment automation

MIT licensed. Issues and pull requests welcome.

---

## Contact

- **Sales and evaluation** — [sales@emiton.eu](mailto:sales@emiton.eu)
- **Technical** — [github@emiton.eu](mailto:github@emiton.eu)

---

<sub>Built by <a href="https://ostv.sk">OSTV</a>, an ISP and broadcast operator in Slovakia (AS209531).</sub>
