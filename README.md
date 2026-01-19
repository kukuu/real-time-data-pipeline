# Real Time Data Pipeline in Distributed Systems

**Workflow**: 

- New Alert Created → POST /api/alerts
- Backend Processes → CorrelationService.correlate()
- Database Save → AlertRepository.save()
- Kafka Event → alert.created (future)
- WebSocket Broadcast → /topic/alerts
- Frontend Receives → useWebSocket hook
- Context Update → AlertContext.setAlerts()
- UI Re-render → Components update
