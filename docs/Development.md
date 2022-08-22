# Jira Development

    ❯ more /private/etc/hosts

    ##
    # Host Database
    #
    # localhost is used to configure the loopback interface
    # when the system is booting.  Do not change this entry.
    ##
    127.0.0.1       localhost
    255.255.255.255 broadcasthost
    ::1             localhost
    127.0.0.1 host.docker.internal

Jmake

    ❯ ./jmake debug -J "-Dcom.sun.management.jmxremote -Dcom.sun.management.jmxremote.port=8199 -Dcom.sun.management.jmxremote.authenticate=false -Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.host=host.docker.internal -Djava.rmi.server.hostname=host.docker.internal"

Docker

    ❯ cd docker
    ❯ docker-compose up --remove-orphans