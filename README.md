# knf-curl
knf crul application

Copyright (C) 2018 KUMINDU INDURANGA RANAWAKA
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
       
        
          KnfCurlHandler knfp=new KnfCurlHandler();

          knfp.COMMAND.add("curl");
          knfp.COMMAND.add("-k");
          knfp.COMMAND.add("-i");
          knfp.COMMAND.add("-d");
          knfp.COMMAND.add("grant_type=password&username=admin&password=admin");
          knfp.COMMAND.add("-H");
          knfp.COMMAND.add("Authorization:token");
          knfp.COMMAND.add("https://127.0.0.1:8000/");

          knfp.Process();

          System.out.println(knfp.getContent());
          System.out.println(knfp.getresponseCode());
          System.out.println(knfp.getValue("token_type"));
        
