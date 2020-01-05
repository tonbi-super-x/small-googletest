
# makeの完全な事項コマンドが見える。デバッグ用
set(CMAKE_VERBOSE_MAKEFILE 1)

# CMakeのバージョンを設定
cmake_minimum_required(VERSION 3.10)

# プロジェクト名と使用する言語を設定
project(test_cmake CXX)


# specify the C++ standard
# set(CMAKE_CXX_STANDARD 11)

# コンパイラーを指定したいとき
set(CMAKE_CXX_COMPILER g++) # なぜかこれをしないとC++ の機能が使えなかった
#set(CMAKE_CXX_COMPILER clang++)

# add_definitions("-Wall -std=c++11") # <= new
# a.outという実行ファイルをmain.cppとhello.cppから作成
add_executable(a.out hello.cpp main.cpp)