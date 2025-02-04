<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

[![License: GPL v2](https://img.shields.io/badge/License-GPL_v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)


# Why use dataspoon?


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/CentralFloridaAttorney/dbtool">
    <img src="images/onehotdb.png" alt="Logo" width="1280" height="480">
  </a>
<h3 align="center">dataspoon</h3>
  <p align="center">
    easy to use tools for working with data
    <br />
    <a href="https://github.com/CentralFloridaAttorney/dataspoon/wiki"><strong>Explore the Wiki»</strong></a>
    <br />
    <a href="https://github.com/CentralFloridaAttorney/dbtool">View Demo | </a>
    <a href="https://github.com/CentralFloridaAttorney/dbtool/issues">Report Bug | </a>
    <a href="https://github.com/CentralFloridaAttorney/dbtool/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
        </li>
        <li>
          <a href="#getting-started">Getting Started</a>
          <ul>
            <li><a href="#prerequisites">Prerequisites</a></li>
            <li><a href="#installation">Installation</a></li>
          </ul>
        </li>
        <li><a href="#usage">Usage</a></li>
        <li><a href="#roadmap">Roadmap</a></li>
        <li><a href="#contributing">Contributing</a></li>
        <li><a href="#license">License</a></li>
        <li><a href="#contact">Contact</a></li>
        <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With


<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started With dataspoon

### dbtool helps you to eat more data
DBTool provides a simple way to connect to a MySQL database

# Explanation of what the code does
 1) create a database
 2) create a table
 3) create a row
 4) create a column
 5) create a value
 6) create a key
 7) create a link_key


DBTool() allows you to create and modify MySQL databases using Python with simple get and put commands.

For example, you can set and get a key/value pair to ('ala'/'kazam') in a row that is referenced by the link_key ('xyzzy'):

````
DBTool().put('xyzzy', 'ala', 'kazam')
value = DBTool().get('xyzzy', 'ala')
````
To perform the same operation in a different database ('magicdb'):
````
DBTool('magicdb').put('xyzzy', 'ala', 'kazam')
value = DBTool('magicdb').get('xyzzy', 'ala')
````

And, to perform the same operation in a different database ('magic_carpet') and a different table ('magic_table')
````
DBTool('magic_carpet', 'magic_table').put('xyzzy', 'ala', 'kazam')
value = DBTool('magic_carpet', 'magic_table').get('xyzzy', 'ala')
````
The behavior of the put method differs depending on the number of parameters passed.

````
    def put(self, primary_key, element_key=None, value=None):
        # 1 parameter: add _link_key (returns row_number of _link_key)
        # 3 parameters: for primary_key set key/value (returns row_number of _link_key)
````


Examples of using DBTool

````
    xyzzydb = DBTool() creates a database named dBTool with table named default_table.
    xyzzydb = DBTool('xyzzydb') creates a database named xyzzydb with a table named default_table.
    xyzzydb = DBTool('xyzzydb', 'best_magic_table') creates a database named xyzzydb with a table named best_magic_table.
    xyzzydb.put('link_key_xyzzy') creates a row with link_key ('link_key_xyzzy')
    xyzzydb.put('other_link_key', 'ala', 'kazam') sets key ('ala') to value ('kazam') in row with link_key ('other_link_key')
    
    1. Create a database ('xyzzydb', 'magic_table'): xyzzydb = DBTool('xyzzydb', 'magic_table').  The MySQL.table_name is a default name, unless you specify a table_name during creation (ex. xyzzydb = DBTool('xyzzydb', 'magic_table')) or after creation (ex. xyzzydb.open_table('new_magic_table'))
    2. Create a new row with a link_key ('link_key_xyzzy'): xyzzydb.put('link_key_xyzzy')
    3. Create or insert into a row with link_key_destination from link_key_source: xyzzydb.put('link_key_source', 'link_key_destination')
    4. Put key/value ('ala'/'kazam') into row with link_key ('link_key_destination'): xyzzydb.put('link_key_destination', 'ala', 'kazam')
    5. Get this_value ('kazam') using key ('ala') from row with link_key_destination : this_value = xyzzydb.get('link_key_destination', 'ala')
    6. Save xyzzydb.magic_table as a pandas.DataFrame .pkl file to location ('data/mysql.pkl'): xyzzydb.pickle_words('data/mysql.pkl')
````
### dbtool.OneHotWords()

# Explanation of what the code does
 1. Create a new instance of the OneHotWords class
 2. Get the index of the word 'hello'
 3. Get the word at index 1
 4. Get all the words in the onehot index


### onehotdb makes data taste better

# Explanation of what the code does
 1) create a new database
 2) create a new table
 3) add a column to the table
 4) add a row to the table
 5) get the row number for a link_key
 6) get the value for a key in a row
 7) get the entire row for a link_key
 8) update a value in a row
 9) delete a table
 10) delete a row
 11) delete a column
 11) delete a database
 12) get the number of rows in a table
 13) get the column names for a table
 14) get a dataframe for a table
 15) get a dataframe for a link_key

### Prerequisites

1. Install MySQL:
    ```
    sudo rm -rf /var/lib/mysql/mysql
    sudo apt-get remove --purge mysql-server mysql-client mysql-common
    sudo apt-get autoremove
    sudo apt-get autoclean
    sudo apt-get install mysql-server
    ```
2. Install mysql-connector-python:
    ```
    pip install mysql-connector-python
    ```
3. Optionally, install mysql-workbench:
    ```
    sudo snap install mysql-workbench-community
    ```

4. You need to know the location (ex. 127.0.0.1 or 192.168.1.69) and port number (ex. 3306 or 50011)
5. You must know the username (ex. 'bilbo') and password (ex. 'baggins') of an authorized user in mysql


### Installation

1. If you need help using dataspoon then [Talk to John](https://centralfloridaattorney.net/schedule-consultation/)
2. Clone the repo
   ```
   git clone https://github.com/CentralFloridaAttorney/dataspoon.git
   ```
3. No NPM packages to install
   ```
   NO npm install
   ```
4. Install mysql packages
   ```
   pip install mysql-connector-python
   ```
5. Create a file named `.env` in the root directory of your project and populate it with the following values:

    ```
    # Used by DBTool
    DBTOOL_USER=bilbo
    DBTOOL_PASSWD=baggins
    DBTOOL_HOST=127.0.0.1
    DBTOOL_PORT=3306
    DBTOOL_DATABASE_NAME=default_database
    DBTOOL_TABLE_NAME=default_table
    DBTOOL_ONEHOTDB_NAME=default_onehotdb
    DBTOOL_ONEHOTDB_TABLE=default_onehotdb_table
    ```
7. Install dotenv:

    ```
    pip install dotenv
    ```


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

   
_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/CentralFloridaAttorney/dbtool/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- TROUBLESHOOTING -->
## Troubleshooting

If you get a root password error when starting MySQL consider: https://askubuntu.com/questions/1406395/mysql-root-password-setup-error

If bilbo is not present then use mysql:
````
create user 'bilbo'@'127.0.0.1' identified by 'baggins';
GRANT ALL PRIVILEGES ON *.* TO 'bilbo'@'127.0.0.1' WITH GRANT OPTION;
show grants for 'bilbo'@'127.0.0.1';
````
If you update Ubuntu and cannot reboot then fix your grub: https://phoenixnap.com/kb/grub-rescue


<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Project Link: [https://github.com/CentralFloridaAttorney/dbtool](https://github.com/CentralFloridaAttorney/dbtool)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#readme-top">back to top</a>)</p>

[![Product Name Screen Shot][product-screenshot]](https://CentralFloridaAttorney.net)


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/CentralFloridaAttorney/dbtool.svg?style=for-the-badge
[contributors-url]: https://github.com/CentralFloridaAttorney/dbtool/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/CentralFloridaAttorney/dbtool.svg?style=for-the-badge
[forks-url]: https://github.com/CentralFloridaAttorney/dbtool/network/members
[stars-shield]: https://img.shields.io/github/stars/CentralFloridaAttorney/dbtool.svg?style=for-the-badge
[stars-url]: https://github.com/CentralFloridaAttorney/dbtool/stargazers
[issues-shield]: https://img.shields.io/github/issues/CentralFloridaAttorney/dbtool.svg?style=for-the-badge
[issues-url]: https://github.com/CentralFloridaAttorney/dbtool/issues
[license-shield]: https://img.shields.io/github/license/CentralFloridaAttorney/dbtool.svg?style=for-the-badge
[license-url]: https://github.com/CentralFloridaAttorney/dbtool/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]:https://www.linkedin.com/in/john-m-iriye-3136478
[product-screenshot]: images/dataspoon_project.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
