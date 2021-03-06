![Backpocket](https://backpocket.cf/git_img/about.png)

Backpocket is a decentralized PoW/PoS cryptocurrency with support for private transactions and high-reward masternodes.
## License
Backpocket implements the guidelines of the [MIT License](https://opensource.org/licenses/MIT). 

## Coin Specificatons 
| Specification | Value |
| ------ | ------ |
| Max Coins | 425M BCKT |
| Block Time | 120 seconds |
| Main Port | 13371 |
| RPC Port | 13370 |
| Masternode Collateral | 42,500 BCKT |
| Algorithm | Scrypt |
| PoS Maturity | 12 hours |

# Installation
## Linux
Add the following dependencies and repositories using APT:
```sh
sudo apt-get install build-essential libssl-dev libboost-all-dev libqrencode-dev pkg-config libminiupnpc-dev qt5-default qttools5-dev-tools libgmp3-dev autoconf automake libtool

sudo add-apt-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install libdb4.8-dev libdb4.8++-dev
```
Clone this github repository and change directory:
```sh
git clone https://github.com/backpocket/backpocket
cd backpocket
```
For compiling the headless backpocketd daemon, enter the following commands:
```sh
cd src
make -f makefile.unix
strip backpocketd
```
For compiling the graphical QT wallet, enter the following commands:
```sh
qmake
make
strip Backpocket-qt
```
To install the daemon and QT wallet globally, copy the files to ```/usr/local/bin``` or whatever path your distro uses.
```sh
sudo cp backpocketd /usr/local/bin
sudo cp Backpocket-qt /usr/local/bin
```

## Windows
Compiliation steps are currently unavailable for Windows operating systems. Compiled wallet downloads are available at [https://backpocket.cf](httsp://backpocket.cf)

# Important
>THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
