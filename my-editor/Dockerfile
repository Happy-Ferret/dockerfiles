FROM ubuntu:14.04

RUN apt-get -y update
RUN apt-get -y install zsh
RUN apt-get -y install git
RUN apt-get -y install ruby
RUN apt-get -y install python
RUN apt-get -y install vim
RUN apt-get -y install tmux
RUN apt-get -y install curl
RUN apt-get -y install wget

RUN useradd marcelo
RUN mkdir /home/marcelo && chown -R marcelo: /home/marcelo

WORKDIR /home/marcelo
ENV HOME /home/marcelo

RUN git clone https://github.com/marceloandrader/dotfiles.git .dotfiles
RUN chown -R marcelo: .dotfiles
RUN git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
RUN chown -R marcelo: .vim
# RUN cd ~/.dotfiles && script/bootstrap -> This need to be run inside the container

EXPOSE 8000
EXPOSE 8001
EXPOSE 8002
EXPOSE 8003

USER marcelo
CMD ["zsh"]
