# TODO: GitHub Pages Setup 📋

## ⚠️ VIGTIGT: DNS skal konfigureres FØRST

GitHub Pages fejl:
```
Both rasmusnielsen.eu and its alternate name are improperly configured
Domain does not resolve to the GitHub Pages server. For more information, see documentation (NotServedByPagesError).
```

## Korrekt rækkefølge: ✅

### ✅ Trin 1: FÆRDIG - Kode uploaded til GitHub
- [x] Repository oprettet: https://github.com/rasmusnielsen-eu/rasmusnielsen.eu
- [x] Kode pushed til main branch
- [x] README.md oprettet

### 🔄 Trin 2: DNS Konfiguration på one.com (SKAL GØRES FØRST!)

**A Records for hoveddomænet:**
```
Type: A
Name: @ 
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A  
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153
```

**CNAME Record for www:**
```
Type: CNAME
Name: www
Value: rasmusnielsen-eu.github.io
```

### ⏳ Trin 3: Vent på DNS propagering
- [ ] Vent 15 minutter - 24 timer
- [ ] Test med: `nslookup rasmusnielsen.eu`
- [ ] Verificer at domænet peger på GitHub's servere

### 🔄 Trin 4: GitHub Pages konfiguration (EFTER DNS)
- [ ] Gå til GitHub repo Settings → Pages
- [ ] Source: "Deploy from a branch"
- [ ] Branch: "main" 
- [ ] Folder: "/ (root)"
- [ ] **EFTER DNS er aktiv:** Tilføj custom domain: `rasmusnielsen.eu`
- [ ] Aktiver "Enforce HTTPS" når det bliver tilgængeligt

### 🎯 Trin 5: Verifikation
- [ ] Test: https://rasmusnielsen.eu
- [ ] Test: https://www.rasmusnielsen.eu  
- [ ] Verificer SSL certifikat
- [ ] Test alle sektioner fungerer

## Nuværende status:
- ✅ Kode er klar på GitHub
- ❌ DNS ikke konfigureret endnu → Dette skal gøres FØRST
- ❌ Custom domain fejler på GitHub Pages

## Næste skridt:
1. **GÅ TIL ONE.COM** og konfigurer DNS records
2. **VENT** på DNS propagering
3. **DEREFTER** tilføj custom domain på GitHub Pages

## Fremtidige projekter:
- [ ] Bryllup subdomæne: `bryllup.rasmusnielsen.eu`
  - Kræver nyt GitHub repository: `rasmusnielsen-eu/bryllup`
  - CNAME record: `bryllup → rasmusnielsen-eu.github.io`

---

📝 **Sidste opdatering:** 2024-12-19  
🔗 **GitHub Repo:** https://github.com/rasmusnielsen-eu/rasmusnielsen.eu 