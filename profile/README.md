# Emiton

**IPTV/OTT platform that runs on one server.**

Headend, transcoding, statistical multiplexing, playout and delivery — a single
box instead of a rack. Built by broadcast engineers who run it in production.

**[Website](https://emiton.eu)** · **[Statmux](https://statmux.eu)** · **[Docs](https://emiton.eu/docs)** · **[Demo](https://emiton.eu/demo)**

---

## What it does

| | |
|---|---|
| **Transcoding** | NVENC/NVDEC hardware pipeline. 30+ channels per node on consumer GPUs. |
| **Statmux** | Software statistical multiplexer with per-frame complexity analysis on CUDA. |
| **Playout** | Scheduled playout, loop channels, ad insertion, deterministic XMLTV EPG. |
| **Delivery** | MPEG-TS multicast, HLS, DASH, SRT, RIST. DVB-C/DVB-T output for cable headends. |
| **Client apps** | White-label RUBIKON apps for Android TV, iOS, Android and web. |
| **Billing** | Metron — CRM, invoicing and subscriber management. |

## Statmux, measured

Statistical multiplexing is usually a hardware purchase. Emiton does it in
software, and the numbers hold up against a CBR baseline on the same transponder:

- **98.4%** transport stream fill at 37.99 Mbps
- **+3.98 VMAF** on the worst-case channel versus constant bitrate
- No dedicated multiplexer hardware

Methodology and full measurement data: **[statmux.eu](https://statmux.eu)**

## Who it's for

Cable operators, IPTV providers and regional broadcasters who need a headend
that fits their scale — not a carrier-grade cluster with a carrier-grade price.

If you are running a DVB-C or DVB-T headend and looking at a six-figure quote
for a statmux, start with the measurements above.

---

## This organization

The platform itself is commercial. What lives here is the open surface around it:

- API specifications and client libraries
- EPG and XMLTV tooling
- TSDuck-based diagnostic scripts
- Prometheus exporters and monitoring integrations
- Deployment automation

MIT licensed, auditable, no black boxes.

---

## Contact

- **Sales and evaluation** — [sales@emiton.eu](mailto:sales@emiton.eu)
- **Technical** — [github@emiton.eu](mailto:github@emiton.eu)

---

<sub>Built by [OSTV](https://ostv.sk), an ISP and broadcast operator in Slovakia (AS209531).
Also from us: [WebMNG](https://github.com/webmng) — hosting control panel licensed per IP.</sub>
