# lfnw
Live code for LinuxFest Northwest 2018

## Install Clojure CLI Tools. More info: https://clojure.org/guides/getting_started

curl -O https://download.clojure.org/install/linux-install-1.9.0.375.sh
chmod +x linux-install-1.9.0.375.sh
sudo ./linux-install-1.9.0.375.sh

## Try the rebel readline lib

https://github.com/bhauman/rebel-readline

clojure -Sdeps "{:deps {com.bhauman/rebel-readline {:mvn/version \"0.1.2\"}}}" -m rebel-readline.main

you can specify an alias in your $HOME/.clojure/deps.edn

{
 ...
 :aliases {:rebel {:extra-deps {com.bhauman/rebel-readline {:mvn/version "0.1.2"}}
                   :main-opts  ["-m" "rebel-readline.main"]}}
}
And then run with a simpler:

    $ clojure -A:rebel
