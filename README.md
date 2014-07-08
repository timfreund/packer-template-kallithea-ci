packer-template-kallithea-ci
============================

This is a [Packer](http://packer.io) template for creating a
[Jenkins](http://jenkins-ci.org/) continuous integration server for
the [Kallithea](https://kallithea-scm.org/) project.

Defining and deploying the server with Packer will allow the team
to quickly rebuild and migrate the service as the needs and personnel
of the project change over time.

This project uses a [Puppet](http://puppetlabs.com/) provisioner to
configure the system with modules defined in the included Puppetfile.
Before building, you will need to download the modules.
[r10k](https://github.com/adrienthebo/r10k) or [librarian-puppet](https://github.com/rodjek/librarian-puppet)
can make that happen:

    $ r10k puppetfile install
