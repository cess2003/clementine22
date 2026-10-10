# Two-Tier Architecture

A two-tier architecture splits an application into two layers that run separately
but work together: an application (web) tier and a database tier.

## The Web/Application Tier
This tier is what users interact with. It serves the user interface, receives and
processes HTTP requests, runs the application logic, and talks to the database
when data is needed. In this lab, the Nextcloud container fills this role.

## The Database Tier
This tier stores persistent data such as user accounts, credentials, and file
metadata. It is responsible for saving, retrieving, and organizing data reliably.
In this lab, the MariaDB container fills this role.

## Why Separate Them?
Separating the web server and database into two containers lets each be updated,
scaled, restarted, or fixed independently without affecting the other. It also
improves security, since the database is not directly exposed to users, and it
follows the principle of one container, one responsibility. A single combined
container would be harder to maintain, troubleshoot, and scale.
