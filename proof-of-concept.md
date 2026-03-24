# Proof of Concept - Symptom Log & Reporter

## Scope
- App category: Social & Community
- Entity model: Symptom Log Community Event
- Deployable stack: Flask + SQLAlchemy + Gunicorn + Docker + CI

## Dynamic Field Configuration
- Host: `host` (text)
- Expected Attendees: `attendees` (number)
- Community Notes: `community_notes` (textarea)

## Run Evidence Commands
```bash
python app.py
curl http://localhost:5000/api/health
curl http://localhost:5000/api/schema
curl -X POST http://localhost:5000/api/records   -H "Content-Type: application/json"   -d '{"title":"Demo Record","status":"open","payload":{"host":"Demo value","attendees":12,"community_notes":"seed note"}}'
curl http://localhost:5000/api/metrics
```

## Metadata
- Idea number: 90
- Generated UTC: 2026-03-24T15:52:22.473447+00:00
- Status: Phase-2 complete
