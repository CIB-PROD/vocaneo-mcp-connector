# Vocaneo MCP Server

**French job profiles, RNCP diplomas and 135,000 training programs. Read-only, no account.**

Vocaneo is the career-guidance platform of [vocaneo.com](https://vocaneo.com). This remote
MCP server exposes its public reference data to AI assistants: 1,500+ job profiles (ROME),
RNCP certifications, training programs across France, training centers, and skills
comparison — in French and English.

- **Server URL**: `https://mcp.vocaneo.com/mcp` (Streamable HTTP, no authentication)
- **Documentation**: [vocaneo.com/connecteur](https://vocaneo.com/connecteur)
- **Privacy policy**: [vocaneo.com/connecteur/confidentialite](https://vocaneo.com/connecteur/confidentialite)
- **Listed on**: [Claude connectors directory](https://claude.ai/directory/connectors/vocaneo) · [official MCP registry](https://registry.modelcontextprotocol.io) (`com.vocaneo/vocaneo`)

All 13 tools are read-only (`readOnlyHint: true`). No account, no API key, no personal data.

## Tools

| Tool | What it does |
|---|---|
| `search_jobs` | Search French job profiles by keyword, sector, salary, accessibility |
| `get_job` | Full job profile: missions, market data, skills (by slug or ROME code) |
| `get_similar_jobs` | Jobs close to a given one |
| `compare_skills` | Compare a person's skills against a target job |
| `list_job_sectors` | The 35 job sectors |
| `get_job_pathways` | Certifications leading to a job, with training aggregates |
| `search_certifications` | Search RNCP/RS certifications |
| `get_certification` | Certification detail |
| `search_trainings` | Search training programs (city, region, CPF eligibility, price, modality...) |
| `get_training` | Training program detail |
| `search_training_centers` | Search training centers and skills-assessment centers |
| `get_training_center` | Training center detail |
| `resolve_location` | Resolve a French postal code or city name to coordinates |

## Use it

**Claude** — add the [Vocaneo connector](https://claude.ai/directory/connectors/vocaneo)
from the directory, or add `https://mcp.vocaneo.com/mcp` as a custom connector.

**Le Chat (Mistral)** — Connectors → Add Connector → Custom MCP Connector →
`https://mcp.vocaneo.com/mcp`.

**Gemini CLI** — this repository is a Gemini CLI extension:

```bash
gemini extensions install https://github.com/CIB-PROD/vocaneo-mcp-connector
```

**Any MCP client** (Streamable HTTP):

```json
{
  "mcpServers": {
    "vocaneo": {
      "url": "https://mcp.vocaneo.com/mcp"
    }
  }
}
```

## Example prompts

- "Quels métiers correspondent à un profil créatif qui aime travailler en extérieur ?"
- "Quelles certifications mènent au métier de développeur web, et où se former à Lyon ?"
- "Compare mes compétences de boulanger avec le métier de pâtissier."
- "Find CPF-eligible data analyst trainings near Marseille."

## À propos (français)

Vocaneo est une plateforme d'orientation professionnelle : bilan d'orientation gratuit,
1 500+ fiches métiers, 135 000 formations, certifications RNCP et établissements partout en
France. Ce serveur MCP expose ce référentiel public aux assistants IA, en lecture seule,
sans compte. Éditeur : VOCANEO SAS, entreprise de l'ESS et société à mission —
[vocaneo.com](https://vocaneo.com).

## Support

Contact: [contact@vocaneo.com](mailto:contact@vocaneo.com)
