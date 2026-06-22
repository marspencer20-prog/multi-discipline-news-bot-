# config/disciplines.py
DISCIPLINES = {
    "land economy": {
        "aliases": ["land economy", "land econ", "土地经济"],
        "auto_keywords": [
            "land use", "land reform", "agricultural land", "farmland",
            "zoning", "spatial planning", "planning permission",
            "housing market", "affordable housing", "social housing",
            "property market", "real estate", "house price",
            "gentrification", "urban sprawl", "green belt",
            "compulsory purchase", "land compensation",
            "natural capital", "ecosystem services", "environmental valuation",
        ],
        "crossref_query": "land economy OR land use OR housing policy OR planning policy",
    },
    "anthropology": {
        "aliases": ["anthropology", "anthropologist", "人类学", "民族学"],
        "auto_keywords": [
            "cultural anthropology", "social anthropology", "ethnography",
            "kinship", "ritual", "symbolism", "myth", "religion",
            "political anthropology", "economic anthropology",
            "medical anthropology", "environmental anthropology",
            "indigenous peoples", "heritage", "museum anthropology",
            "development anthropology", "globalization", "migration",
        ],
        "crossref_query": "anthropology OR ethnography OR cultural anthropology",
    },
    "economics": {
        "aliases": ["economics", "economy", "经济", "宏观经济学"],
        "auto_keywords": [
            "gdp", "inflation", "interest rate", "monetary policy",
            "fiscal policy", "budget deficit", "unemployment",
            "labour market", "wage growth", "exchange rate",
            "bank of england", "treasury", "recession", "productivity",
        ],
        "crossref_query": "economics OR monetary policy OR fiscal policy",
    },
}

def resolve_discipline(raw: str) -> tuple[str, dict]:
    """模糊匹配专业名，返回标准化名称和配置"""
    rl = raw.lower().strip()
    for k, v in DISCIPLINES.items():
        if rl == k or rl in v["aliases"]:
            return k, v
    # 未知专业：兜底（后续手动补）
    return rl, {
        "aliases": [raw],
        "auto_keywords": [raw],
        "crossref_query": raw,
    }
