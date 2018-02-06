# OneMy

OneMy help pages

```C#
Mapper.Initialize(x =>
{
    x.CreateMap<BotUser, CrucialInfo>();
    x.CreateMap<CrucialInfo, BotUser>();

    x.CreateMap<BotUser, OfficialInfo>();
    x.CreateMap<BotUser, DOBInfo>();
    x.CreateMap<BotUser, ContactInfo>();
    x.CreateMap<BotUser, HomeAddress>();
    x.CreateMap<BotUser, OfficeAddress>();
    x.CreateMap<BotUser, Business[]>();
});
```
