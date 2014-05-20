**Important**

This a <s>hack</s> customized fork of the original extension that display the gravatar in the user info. Currently compatible (and tested) with **RT 4.2.3.**

----------

**NAME**
RT::Extension::Gravatar - Adds gravatar images to rt

**DESCRIPTION**
This Plugin adds an gravatar image to the following places:

- More about the requestors widget
- Modify user page
- About me (Preferences)
- User Summary
- User info

**INSTALLATION**

    perl Makefile.PL
    make
    make install

Edit your */opt/rt4/etc/RT_SiteConfig.pm* and add this line:

    Set(@Plugins, qw(RT::Extension::Gravatar));

or add "RT::Extension::Gravatar" to your existing @Plugins line.

 Clear your mason cache
 

    rm -rf /opt/rt4/var/mason_data/obj/*

Restart your webserver

**METHODS ADDED TO OTHER CLASSES**

      RT::User
       GravatarUrl([Size], [Design])
        Return the gravatar image url of the user.
    
       HasGravatar
        Return true if the user has an gravatar image.

**AUTHOR**
Christian Loos <cloos@netsandbox.de>

**LICENCE AND COPYRIGHT**
Copyright (C) 2010-2013, Christian Loos.
    This library is free software; you can redistribute it and/or modify it
    under the same terms as Perl itself.

**SEE ALSO**
    <http://bestpractical.com/rt/>
    <http://gravatar.com/>