# Alex_Puppet_PuppetDB_SVN
Test puppet with puppet DB and SVN

The original purpose to test puppet for automatic ddeploy Cisco nexus DC switches . and final try a total solution ,include puppet agent with gem cisco_utilities inside Nexus OS virtual service .A puppet server with puppet_cisco_module. Also deployed puppetDB for web access puppet server status, fot puppet DB , the most important thing is puppetDB provides REST API. We can query via REST API to build customized application integration with puppet solutions. For puppet code version control , dopoyed SVN for automatic sync up puppet module code , from code developer to SVN server and hooked sync up to puppet server and sync up by puppet agent to nodes.

Logical diagram as following :

Node(puppet agent /Gem utilities) <----->puppet Server(site.pp / modules)<------->Postgre SQL<------>Web server<------>browser
       node report
            ^                                            ^                                                ^
            |                                            |                                                | 
            |---------------------------------------------------------------------------------------------|
                                                         |
                                                         |
                                                 SVN Server(apach 2)
                                                         |
                 Puppet Code Develope< ------------------|
                                                         
                                                         
