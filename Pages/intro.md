Hi!

This is main page.


```C#
#region Tell AutoMapper what can be mapped and use everywhere Mapper.Map bla-bla
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
#endregion Tell AutoMapper what can be mapped and use everywhere Mapper.Map bla-bla
```