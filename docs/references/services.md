---
layout: default
title: uSupport.Services
parent: References
nav_order: 2
---

{: .note }
The documentation is still a work in progress. More details is coming soon.

## uSupportTicketService
```c#
IEnumerable<uSupportTicket> GetAll();
uSupportPage<uSupportTicket> GetPagedResolvedTickets(long page);
uSupportPage<uSupportTicket> GetPagedActiveTickets(long page);
bool AnyResolvedTickets();
uSupportTicket Get(Guid id);
uSupportTicket Create(uSupportTicketSchema ticket);
uSupportTicket Update(uSupportTicketSchema ticketDto);
void Delete(Guid id);
void ClearTicketCache();
```

## uSupportTicketTypeService
```c#
IEnumerable<uSupportTicketType> GetAll();
uSupportTicketType Get(Guid id);
IEnumerable<uSupportTicketType> GetByIds(List<Guid> ids);
Guid GetTypeIdFromName(string name);
uSupportTicketType Create(uSupportTicketTypeSchema ticketType);
uSupportTicketType Update(uSupportTicketTypeSchema ticketType);
void Delete(Guid id);
int GetTypesCount();
```

## uSupportTicketStatusService
```c#
IEnumerable<uSupportTicketStatus> GetAll();
IEnumerable<uSupportTicketStatus> GetResolvedStatuses();
IEnumerable<uSupportTicketStatus> GetActiveStatuses();
uSupportTicketStatus GetDefaultStatus();
uSupportTicketStatus Get(Guid id);
IEnumerable<uSupportTicketStatus> GetByIds(List<Guid> ids);
Guid GetStatusIdFromName(string name);
uSupportTicketStatus Create(uSupportTicketStatusSchema ticketStatus);
uSupportTicketStatus Update(uSupportTicketStatusSchema ticketStatus);
void Delete(Guid id);
int GetStatusCount();
```

## uSupportSettingsService
```c#
void SendEmail(string toAddress, string subject, string templateViewPath, object model);
bool GetSendEmailOnTicketCreatedSetting();
string GetTicketUpdateEmailSetting();
string GetEmailSubjectNewTicket();
string GetEmailSubjectUpdateTicket();
string GetEmailTemplateNewTicketPath();
string GetEmailTemplateUpdateTicketPath();
```

## uSupportTicketCommentService
```c#
IEnumerable<uSupportTicketComment> GetCommentsFromTicketId(Guid ticketId);
uSupportTicketComment Get(Guid id);
uSupportTicketComment Create(uSupportTicketCommentSchema comment);
uSupportTicketComment Update(uSupportTicketCommentSchema comment);
void Delete(Guid id);
```