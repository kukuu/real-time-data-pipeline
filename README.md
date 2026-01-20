# Real Time Data Pipeline in Distributed Systems

**Workflow**: 

- New Alert Created → eg. POST /api/alerts
- Backend Processes → eg CorrelationService.correlate()
- Database Save → eg AlertRepository.save()
- Kafka Event → eg alert.created (future)
- WebSocket Broadcast → eg /topic/alerts
- Frontend Receives → eg useWebSocket hook
- Context Update → eg AlertContext.setAlerts()
- UI Re-render → eg Components update 
