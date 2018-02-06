OneMy
=====

OneMy help pages
----------------

Code::

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

.. Tip:: The library ``unittest.mock`` was introduced on python 3.3. On earlier versions install the ``mock`` library
    from PyPI with (ie ``pip install mock``) and replace the above import::

        from mock import Mock as MagicMock

If such libraries are installed via ``setup.py``, you also will need to remove all the C-dependent libraries from your ``install_requires`` in the RTD environment.

`Client Error 401` when building documentation
----------------------------------------------

If you did not install the `test_data` fixture during the installation
instructions, you will get the following error::

    slumber.exceptions.HttpClientError: Client Error 401: http://localhost:8000/api/v1/version/

This is because the API admin user does not exist, and so cannot authenticate.
You can fix this by loading the test_data::

    ./manage.py loaddata test_data

If you'd prefer not to install the test data, you'll need to provide a database
account for the builder to use. You can provide these credentials by editing the
following settings::

    SLUMBER_USERNAME = 'test'
    SLUMBER_PASSWORD = 'test'
