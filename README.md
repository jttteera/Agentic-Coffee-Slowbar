# Agentic Coffee Slow Bar

Coffee RAG web application with two routes: `/` and `/chat`. Current implementation: HTML/CSS/JavaScript + Python, PostgreSQL, LightRAG and Gemini in Docker. AI reads the current catalog and knowledge; authenticated staff can prepare and confirm catalog changes inline in chat.

- [Run the app and try AI tools](app/README.md)
- [Thai mock shop handbook: 16-page PDF](output/pdf/agentic-coffee-shop-handbook.pdf) / [editable text](docs/mock/handbook/handbook.md) / [extracted PDF text](output/pdf/agentic-coffee-shop-handbook.txt)
- [Knowledge and AI tools delivery report](docs/planning/knowledge-tools-007.md)

The design links and planning snapshots below are historical; they do not describe current runtime verification.

1. Ask in Thai about the shop, beans, roast levels and brewing; answers cite the approved knowledge.
2. Within the chat: choose coffee → method/quantity/service → review quote → request pickup date/time → receive an inline pending-confirmation receipt.
3. Attach a handwritten coffee note in the same chat composer → correct its inline OCR draft → continue in the same conversation.

- [Current Figma: Landing](https://www.figma.com/design/sshfWtNKne9n6ilBMX7oBE/Untitled?node-id=3-2427) / [Chatbot](https://www.figma.com/design/sshfWtNKne9n6ilBMX7oBE/Untitled?node-id=3-2501) / [web flow board](https://www.figma.com/design/sshfWtNKne9n6ilBMX7oBE/Untitled?node-id=3-2422)
- [Current static gallery](docs/design/web-v4/preview.html)
- [Independent design review](docs/design/web-v4/independent-review.md) / [Interaction contract](docs/design/web-v4/interaction-contract.md)
- [Research and design choices](docs/design/web-v3/research.md)
- [Figma handoff and verified limits](docs/design/web-v4/figma-handoff.md) / [theme tokens](docs/design/web-v4/material-tokens.json)
- [Customer scope, stack, API and capacity plan](docs/planning/scope-and-api.md)
- [Course rubric mapping](docs/planning/rubric-mapping.md) / [test plan](docs/planning/test-plan.md)
- [Architecture](docs/planning/architecture.png) / [one-message data flow](docs/planning/message-dataflow.png)
- [Mock knowledge PDF, 8 pages](output/pdf/agentic-coffee-mock-knowledge.pdf) / [source](docs/mock/knowledge-mock.md) / [synthetic catalog](docs/mock/catalog.demo.json)

Earlier stack proposal was Next.js; the implemented stack follows the later HTML/Python request. See `app/README.md` for current setup and provider evidence.

There is no management dashboard, payment, POS, inventory automation or table booking. Catalog-only staff tools and authenticated confirmation APIs were added in task 007. A receipt acknowledges a stored request; it does not confirm a reservation or fulfillment. Shop confirmation is a business policy outside this customer prototype. Availability uses seeded demo schedule fixtures.

Catalog, prices, opening hours, timings, images and queue examples are synthetic. Do not commit real customer data, uploaded images or credentials. The generated hero is a concept asset, not a photograph of an operating shop. Native Figma text/vectors were verified; the file is not a .fig backup. Exactly two routes: `/` Landing and `/chat` Chatbot. The prior 12-screen and mobile journey boards are hidden and superseded by web-v4. Earlier design files are historical only.

## Prior local design refinement

[avoid-ai-design v5 before/after preview](docs/design/web-v5/preview.html) · [audit](docs/design/web-v5/audit.md) · [handoff](docs/design/web-v5/handoff.md). Six main views refined; prior conversation states and flow remain in v4. Local PNG/SVG review passed; Figma v5 import is pending/unverified after browser connection loss. Links above to Figma still refer to the last verified v4 delivery.

## Latest local design: logo and chat gallery

[v6 interactive design preview](docs/design/web-v6/preview.html) · [logo](docs/design/web-v6/assets/logo-mark.png) · [original slow-bar quotes](docs/design/web-v6/quotes.md) · [gallery contract and limits](docs/design/web-v6/handoff.md). Five beans can be filtered and selected from chat, then method/quantity/service adjusted in the same conversation. Responsive web inspected at 1440/1024/390; 22 baseline UI-demo checks passed. [D03 Landing-to-chat keyboard focus](docs/design/web-v6/D03-correction.md) subsequently corrected and owner-verified at1440/390; the corrected source awaits any independently requested review. No real order/RAG/OCR services. Figma v6 transfer is pending: current connector lacks edit access or requires reauthentication; links above still show the last verified v4.
