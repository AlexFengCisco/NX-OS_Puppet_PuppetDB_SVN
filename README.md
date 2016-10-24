# Alex_Puppet_PuppetDB_SVN
Test puppet with puppet DB and SVN

The original purpose to test puppet for automatic deploy Cisco nexus DC switches . and finally try a total solution ,includes puppet agent with gem cisco_utilities inside Nexus OS virtual service .A puppet server with puppet_cisco_module. Also deployed puppetDB for web access puppet server status, fot puppet DB , the most important thing is puppetDB provides REST API. We can query via REST API to build customized application integration with puppet solutions. For puppet code version control , deployed SVN for automatic sync up puppet module code , from code developer to SVN server and hooked sync up to puppet server and sync up by puppet agent to nodes.

Logical diagram as following :


                                                                   Postgre SQL
                                                                        |
                                                                        |
     Node(puppet agent) <---->puppet Server(site.pp / modules)<----->Puppet DB
    Gem Utilities                       ^                               ^
       node report                      |                               |
            ^                           |                               |
            |                           |                               | 
            |-----------------------------------------------------------|
                                        |                               |
                                        |                               | 
                             SVN Server(http/SVN)       Apache2 Web Server/REST API 
                                        |                               |
                                        |                               |
                               Code Developer               Web Browser/Application
          
                                                         


Prepared By Alex Feng Oct,2016                                                         
