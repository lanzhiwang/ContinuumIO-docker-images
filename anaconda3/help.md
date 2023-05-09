# conda

conda 是一个包管理工具及 python 环境管理工具。它的第一个作用是用来管理 python 包，相当于 pip 的升级版本；第二个作用是可以用来创建虚拟环境从而可以在一台终端创建多个 python 版本或 python 软件包及其依赖环境。

当然除了 python 外，conda 还可以管理 R。

conda的 特点是免费，开源，跨平台。

miniconda 和 anacnoda 是 conda 的发型版本，关系类似于 ubuntu 和 centos 是 linux 的发行版本。

miniconda 是 conda 的一个小型发行（安装）版本。它只包含 conda，python，少量依赖包，以及少量工具如 pip、zlip。miniconda 的特点是免费，开源，跨平台。

anaconda 是 conda 的一个大型发型（安装）版本。它包含 conda，conda-build，python，250+ 预安装的用于科学计算的包及其依赖，包括 SciPy，NumPy 等等。除了命令行工具外，anaconda 还有桌面应用 Anaconda Navigator 等等。anaconda 的特点是个人免费，开源，跨平台。

# Mamba

Mamba 是一个快速、强大且跨平台的包管理器。

它运行在 Windows、OS X 和 Linux（包括 ARM64 和 PPC64LE）上，完全兼容 conda 包，支持 conda 的大部分命令。

mamba-org 组织拥有多种 Mamba 风格：

* mamba：一个基于 Python 的 CLI，被认为是 conda 的直接替代品，提供更快的速度和更可靠的环境解决方案

* micromamba：一个基于纯 C++ 的 CLI，独立于单个文件可执行文件中

* libmamba：一个 C++ 库，公开低级和高级 API，在其上构建了 mamba 和 micromamba

```bash
$ conda --help
usage: conda [-h] [-V] command ...

conda is a tool for managing and deploying applications, environments and packages.

Options:

positional arguments:
  command
    clean             Remove unused packages and caches.
                      删除未使用的包和缓存。

    compare           Compare packages between conda environments.
                      比较 conda 环境之间的包。

    config            Modify configuration values in .condarc. This is modeled after the git config command. Writes to the user .condarc file
                      (/root/.condarc) by default. Use the --show-sources flag to display all identified configuration locations on your computer.
                      修改 .condarc 中的配置值。 这是在 git config 命令之后建模的。
                      默认写入用户 .condarc 文件 (/root/.condarc)。
                      使用 --show-sources 标志显示计算机上所有已

    create            Create a new conda environment from a list of specified packages.

    info              Display information about current conda install.

    init              Initialize conda for shell interaction.
                      初始化 conda 以进行 shell 交互。

    install           Installs a list of packages into a specified conda environment.

    list              List installed packages in a conda environment.

    package           Low-level conda package utility. (EXPERIMENTAL)实验性的

    remove (uninstall)
                      Remove a list of packages from a specified conda environment. Use `--all` flag to remove all packages and the environment itself.

    rename            Renames an existing environment.

    run               Run an executable in a conda environment.

    search            Search for packages and display associated information.The input is a MatchSpec, a query language for conda packages.
                      See examples below.

    update (upgrade)  Updates conda packages to the latest compatible version.

    notices           Retrieves latest channel notifications.

options:
  -h, --help          Show this help message and exit.
  -V, --version       Show the conda version number and exit.

conda commands available from other packages (legacy):
  build
  content-trust
  convert
  debug
  develop
  env
  index
  inspect
  metapackage
  pack
  render
  repo
  server
  skeleton
  token
  verify
$


$ conda config --show-sources

$

$ conda info

     active environment : base
    active env location : /opt/conda
            shell level : 1
       user config file : /root/.condarc
 populated config files :
          conda version : 23.3.1
    conda-build version : 3.24.0
         python version : 3.10.9.final.0
       virtual packages : __archspec=1=x86_64
                          __glibc=2.31=0
                          __linux=5.15.49=0
                          __unix=0=0
       base environment : /opt/conda  (writable)
      conda av data dir : /opt/conda/etc/conda
  conda av metadata url : None
           channel URLs : https://repo.anaconda.com/pkgs/main/linux-64
                          https://repo.anaconda.com/pkgs/main/noarch
                          https://repo.anaconda.com/pkgs/r/linux-64
                          https://repo.anaconda.com/pkgs/r/noarch
          package cache : /opt/conda/pkgs
                          /root/.conda/pkgs
       envs directories : /opt/conda/envs
                          /root/.conda/envs
               platform : linux-64
             user-agent : conda/23.3.1 requests/2.28.1 CPython/3.10.9 Linux/5.15.49-linuxkit debian/11 glibc/2.31
                UID:GID : 0:0
             netrc file : None
           offline mode : False

$

$ conda list
# packages in environment at /opt/conda:
#
# Name                    Version                   Build  Channel
_libgcc_mutex             0.1                        main
_openmp_mutex             5.1                       1_gnu
alabaster                 0.7.12             pyhd3eb1b0_0
anaconda-client           1.11.2          py310h06a4308_0
anaconda-navigator        2.4.0           py310h06a4308_0
anaconda-project          0.11.1          py310h06a4308_0
anyio                     3.5.0           py310h06a4308_0
appdirs                   1.4.4              pyhd3eb1b0_0
argon2-cffi               21.3.0             pyhd3eb1b0_0
argon2-cffi-bindings      21.2.0          py310h7f8727e_0
arrow                     1.2.3           py310h06a4308_1
astroid                   2.14.2          py310h06a4308_0
astropy                   5.1             py310ha9d4c09_0
asttokens                 2.0.5              pyhd3eb1b0_0
atomicwrites              1.4.0                      py_0
attrs                     22.1.0          py310h06a4308_0
automat                   20.2.0                     py_0
autopep8                  1.6.0              pyhd3eb1b0_1
babel                     2.11.0          py310h06a4308_0
backcall                  0.2.0              pyhd3eb1b0_0
backports                 1.1                pyhd3eb1b0_0
backports.functools_lru_cache 1.6.4              pyhd3eb1b0_0
backports.tempfile        1.0                pyhd3eb1b0_1
backports.weakref         1.0.post1                  py_1
bcrypt                    3.2.0           py310h5eee18b_1
beautifulsoup4            4.11.1          py310h06a4308_0
binaryornot               0.4.4              pyhd3eb1b0_1
black                     22.6.0          py310h06a4308_0
blas                      1.0                         mkl
bleach                    4.1.0              pyhd3eb1b0_0
blosc                     1.21.3               h6a678d5_0
bokeh                     2.4.3           py310h06a4308_0
boltons                   23.0.0          py310h06a4308_0
bottleneck                1.3.5           py310ha9d4c09_0
brotli                    1.0.9                h5eee18b_7
brotli-bin                1.0.9                h5eee18b_7
brotlipy                  0.7.0           py310h7f8727e_1002
brunsli                   0.1                  h2531618_0
bzip2                     1.0.8                h7b6447c_0
c-ares                    1.18.1               h7f8727e_0
ca-certificates           2023.01.10           h06a4308_0
certifi                   2022.12.7       py310h06a4308_0
cffi                      1.15.1          py310h5eee18b_3
cfitsio                   3.470                h5893167_7
chardet                   4.0.0           py310h06a4308_1003
charls                    2.2.0                h2531618_0
charset-normalizer        2.0.4              pyhd3eb1b0_0
click                     8.0.4           py310h06a4308_0
cloudpickle               2.0.0              pyhd3eb1b0_0
clyent                    1.2.2           py310h06a4308_1
colorama                  0.4.6           py310h06a4308_0
colorcet                  3.0.1           py310h06a4308_0
comm                      0.1.2           py310h06a4308_0
conda                     23.3.1          py310h06a4308_0
conda-build               3.24.0          py310h06a4308_0
conda-content-trust       0.1.3           py310h06a4308_0
conda-pack                0.6.0              pyhd3eb1b0_0
conda-package-handling    2.0.2           py310h06a4308_0
conda-package-streaming   0.7.0           py310h06a4308_0
conda-repo-cli            1.0.41          py310h06a4308_0
conda-token               0.4.0              pyhd3eb1b0_0
conda-verify              3.4.2                      py_1
constantly                15.1.0          py310h06a4308_0
contourpy                 1.0.5           py310hdb19cb5_0
cookiecutter              1.7.3              pyhd3eb1b0_0
cryptography              39.0.1          py310h9ce1e76_0
cssselect                 1.1.0              pyhd3eb1b0_0
curl                      7.87.0               h5eee18b_0
cycler                    0.11.0             pyhd3eb1b0_0
cytoolz                   0.12.0          py310h5eee18b_0
daal4py                   2023.0.2        py310h3c18c91_0
dal                       2023.0.1         hdb19cb5_26647
dask                      2022.7.0        py310h06a4308_0
dask-core                 2022.7.0        py310h06a4308_0
datashader                0.14.4          py310h06a4308_0
datashape                 0.5.4           py310h06a4308_1
dbus                      1.13.18              hb2f20db_0
debugpy                   1.5.1           py310h295c915_0
decorator                 5.1.1              pyhd3eb1b0_0
defusedxml                0.7.1              pyhd3eb1b0_0
diff-match-patch          20200713           pyhd3eb1b0_0
dill                      0.3.6           py310h06a4308_0
distributed               2022.7.0        py310h06a4308_0
docstring-to-markdown     0.11            py310h06a4308_0
docutils                  0.18.1          py310h06a4308_3
entrypoints               0.4             py310h06a4308_0
et_xmlfile                1.1.0           py310h06a4308_0
executing                 0.8.3              pyhd3eb1b0_0
expat                     2.4.9                h6a678d5_0
filelock                  3.9.0           py310h06a4308_0
flake8                    6.0.0           py310h06a4308_0
flask                     2.2.2           py310h06a4308_0
flit-core                 3.6.0              pyhd3eb1b0_0
fontconfig                2.14.1               h52c9d5c_1
fonttools                 4.25.0             pyhd3eb1b0_0
freetype                  2.12.1               h4a9f257_0
fsspec                    2022.11.0       py310h06a4308_0
future                    0.18.3          py310h06a4308_0
gensim                    4.3.0           py310h1128e8f_0
giflib                    5.2.1                h5eee18b_3
glib                      2.69.1               he621ea3_2
glob2                     0.7                pyhd3eb1b0_0
gmp                       6.2.1                h295c915_3
gmpy2                     2.1.2           py310heeb90bb_0
greenlet                  2.0.1           py310h6a678d5_0
gst-plugins-base          1.14.1               h6a678d5_1
gstreamer                 1.14.1               h5eee18b_1
h5py                      3.7.0           py310he06866b_0
hdf5                      1.10.6               h3ffc7dd_1
heapdict                  1.0.1              pyhd3eb1b0_0
holoviews                 1.15.4          py310h06a4308_0
huggingface_hub           0.10.1          py310h06a4308_0
hvplot                    0.8.2           py310h06a4308_0
hyperlink                 21.0.0             pyhd3eb1b0_0
icu                       58.2                 he6710b0_3
idna                      3.4             py310h06a4308_0
imagecodecs               2021.8.26       py310h46e8fbd_2
imageio                   2.26.0          py310h06a4308_0
imagesize                 1.4.1           py310h06a4308_0
imbalanced-learn          0.10.1          py310h06a4308_0
importlib-metadata        4.11.3          py310h06a4308_0
importlib_metadata        4.11.3               hd3eb1b0_0
incremental               21.3.0             pyhd3eb1b0_0
inflection                0.5.1           py310h06a4308_0
iniconfig                 1.1.1              pyhd3eb1b0_0
intake                    0.6.7           py310h06a4308_0
intel-openmp              2021.4.0          h06a4308_3561
intervaltree              3.1.0              pyhd3eb1b0_0
ipykernel                 6.19.2          py310h2f386ee_0
ipython                   8.10.0          py310h06a4308_0
ipython_genutils          0.2.0              pyhd3eb1b0_1
ipywidgets                7.6.5              pyhd3eb1b0_1
isort                     5.9.3              pyhd3eb1b0_0
itemadapter               0.3.0              pyhd3eb1b0_0
itemloaders               1.0.4              pyhd3eb1b0_1
itsdangerous              2.0.1              pyhd3eb1b0_0
jedi                      0.18.1          py310h06a4308_1
jeepney                   0.7.1              pyhd3eb1b0_0
jellyfish                 0.9.0           py310h7f8727e_0
jinja2                    3.1.2           py310h06a4308_0
jinja2-time               0.2.0              pyhd3eb1b0_3
jmespath                  0.10.0             pyhd3eb1b0_0
joblib                    1.1.1           py310h06a4308_0
jpeg                      9e                   h5eee18b_1
jq                        1.6               h27cfd23_1000
json5                     0.9.6              pyhd3eb1b0_0
jsonpatch                 1.32               pyhd3eb1b0_0
jsonpointer               2.1                pyhd3eb1b0_0
jsonschema                4.17.3          py310h06a4308_0
jupyter                   1.0.0           py310h06a4308_8
jupyter_client            7.3.4           py310h06a4308_0
jupyter_console           6.6.2           py310h06a4308_0
jupyter_core              5.2.0           py310h06a4308_0
jupyter_server            1.23.4          py310h06a4308_0
jupyterlab                3.5.3           py310h06a4308_0
jupyterlab_pygments       0.1.2                      py_0
jupyterlab_server         2.19.0          py310h06a4308_0
jupyterlab_widgets        1.0.0              pyhd3eb1b0_1
jxrlib                    1.1                  h7b6447c_2
keyring                   23.4.0          py310h06a4308_0
kiwisolver                1.4.4           py310h6a678d5_0
krb5                      1.19.4               h568e23c_0
lazy-object-proxy         1.6.0           py310h7f8727e_0
lcms2                     2.12                 h3be6417_0
ld_impl_linux-64          2.38                 h1181459_1
lerc                      3.0                  h295c915_0
libaec                    1.0.4                he6710b0_1
libarchive                3.6.2                hab531cd_0
libbrotlicommon           1.0.9                h5eee18b_7
libbrotlidec              1.0.9                h5eee18b_7
libbrotlienc              1.0.9                h5eee18b_7
libclang                  10.0.1          default_hb85057a_2
libcurl                   7.87.0               h91b91d3_0
libdeflate                1.17                 h5eee18b_0
libedit                   3.1.20221030         h5eee18b_0
libev                     4.33                 h7f8727e_1
libevent                  2.1.12               h8f2d780_0
libffi                    3.4.2                h6a678d5_6
libgcc-ng                 11.2.0               h1234567_1
libgfortran-ng            11.2.0               h00389a5_1
libgfortran5              11.2.0               h1234567_1
libgomp                   11.2.0               h1234567_1
liblief                   0.12.3               h6a678d5_0
libllvm10                 10.0.1               hbcb73fb_5
libllvm11                 11.1.0               h9e868ea_6
libnghttp2                1.46.0               hce63b2e_0
libpng                    1.6.39               h5eee18b_0
libpq                     12.9                 h16c4e8d_3
libprotobuf               3.20.3               he621ea3_0
libsodium                 1.0.18               h7b6447c_0
libspatialindex           1.9.3                h2531618_0
libssh2                   1.10.0               h8f2d780_0
libstdcxx-ng              11.2.0               h1234567_1
libtiff                   4.5.0                h6a678d5_2
libuuid                   1.41.5               h5eee18b_0
libwebp                   1.2.4                h11a3e52_1
libwebp-base              1.2.4                h5eee18b_1
libxcb                    1.15                 h7f8727e_0
libxkbcommon              1.0.1                hfa300c1_0
libxml2                   2.9.14               h74e7548_0
libxslt                   1.1.35               h4e12654_0
libzopfli                 1.0.3                he6710b0_0
llvmlite                  0.39.1          py310he621ea3_0
locket                    1.0.0           py310h06a4308_0
lxml                      4.9.1           py310h1edc446_0
lz4                       3.1.3           py310h7f8727e_0
lz4-c                     1.9.4                h6a678d5_0
lzo                       2.10                 h7b6447c_2
markdown                  3.4.1           py310h06a4308_0
markupsafe                2.1.1           py310h7f8727e_0
matplotlib                3.7.0           py310h06a4308_0
matplotlib-base           3.7.0           py310h1128e8f_0
matplotlib-inline         0.1.6           py310h06a4308_0
mccabe                    0.7.0              pyhd3eb1b0_0
mistune                   0.8.4           py310h7f8727e_1000
mkl                       2021.4.0           h06a4308_640
mkl-service               2.4.0           py310h7f8727e_0
mkl_fft                   1.3.1           py310hd6ae3a3_0
mkl_random                1.2.2           py310h00e6091_0
mock                      4.0.3              pyhd3eb1b0_0
mpc                       1.1.0                h10f8cd9_1
mpfr                      4.0.2                hb69a4c5_1
mpi                       1.0                       mpich
mpich                     3.3.2                external_0
mpmath                    1.2.1                    pypi_0    pypi
msgpack-python            1.0.3           py310hd09550d_0
multipledispatch          0.6.0           py310h06a4308_0
munkres                   1.1.4                      py_0
mypy_extensions           0.4.3           py310h06a4308_0
navigator-updater         0.3.0           py310h06a4308_0
nbclassic                 0.5.2           py310h06a4308_0
nbclient                  0.5.13          py310h06a4308_0
nbconvert                 6.5.4           py310h06a4308_0
nbformat                  5.7.0           py310h06a4308_0
ncurses                   6.4                  h6a678d5_0
nest-asyncio              1.5.6           py310h06a4308_0
networkx                  2.8.4           py310h06a4308_0
ninja                     1.10.2               h06a4308_5
ninja-base                1.10.2               hd09550d_5
nltk                      3.7                pyhd3eb1b0_0
notebook                  6.5.2           py310h06a4308_0
notebook-shim             0.2.2           py310h06a4308_0
nspr                      4.33                 h295c915_0
nss                       3.74                 h0370c37_0
numba                     0.56.4          py310h1128e8f_0
numexpr                   2.8.4           py310h8879344_0
numpy                     1.23.5          py310hd5efca6_0
numpy-base                1.23.5          py310h8e6c178_0
numpydoc                  1.5.0           py310h06a4308_0
oniguruma                 6.9.7.1              h27cfd23_0
openjpeg                  2.4.0                h3ad879b_0
openpyxl                  3.0.10          py310h5eee18b_0
openssl                   1.1.1t               h7f8727e_0
packaging                 22.0            py310h06a4308_0
pandas                    1.5.3           py310h1128e8f_0
pandocfilters             1.5.0              pyhd3eb1b0_0
panel                     0.14.3          py310h06a4308_0
param                     1.12.3          py310h06a4308_0
parsel                    1.6.0           py310h06a4308_0
parso                     0.8.3              pyhd3eb1b0_0
partd                     1.2.0              pyhd3eb1b0_1
patch                     2.7.6             h7b6447c_1001
patchelf                  0.17.2               h6a678d5_0
pathlib                   1.0.1              pyhd3eb1b0_1
pathspec                  0.10.3          py310h06a4308_0
patsy                     0.5.3           py310h06a4308_0
pcre                      8.45                 h295c915_0
pep8                      1.7.1           py310h06a4308_1
pexpect                   4.8.0              pyhd3eb1b0_3
pickleshare               0.7.5           pyhd3eb1b0_1003
pillow                    9.4.0           py310h6a678d5_0
pip                       22.3.1          py310h06a4308_0
pkginfo                   1.9.6           py310h06a4308_0
platformdirs              2.5.2           py310h06a4308_0
plotly                    5.9.0           py310h06a4308_0
pluggy                    1.0.0           py310h06a4308_1
ply                       3.11            py310h06a4308_0
pooch                     1.4.0              pyhd3eb1b0_0
poyo                      0.5.0              pyhd3eb1b0_0
prometheus_client         0.14.1          py310h06a4308_0
prompt-toolkit            3.0.36          py310h06a4308_0
prompt_toolkit            3.0.36               hd3eb1b0_0
protego                   0.1.16                     py_0
psutil                    5.9.0           py310h5eee18b_0
ptyprocess                0.7.0              pyhd3eb1b0_2
pure_eval                 0.2.2              pyhd3eb1b0_0
py                        1.11.0             pyhd3eb1b0_0
py-lief                   0.12.3          py310h6a678d5_0
pyasn1                    0.4.8              pyhd3eb1b0_0
pyasn1-modules            0.2.8                      py_0
pycodestyle               2.10.0          py310h06a4308_0
pycosat                   0.6.4           py310h5eee18b_0
pycparser                 2.21               pyhd3eb1b0_0
pyct                      0.5.0           py310h06a4308_0
pycurl                    7.45.1          py310h8f2d780_0
pydispatcher              2.0.5           py310h06a4308_2
pydocstyle                6.3.0           py310h06a4308_0
pyerfa                    2.0.0           py310h7f8727e_0
pyflakes                  3.0.1           py310h06a4308_0
pygments                  2.11.2             pyhd3eb1b0_0
pyhamcrest                2.0.2              pyhd3eb1b0_2
pyjwt                     2.4.0           py310h06a4308_0
pylint                    2.16.2          py310h06a4308_0
pylint-venv               2.3.0           py310h06a4308_0
pyls-spyder               0.4.0              pyhd3eb1b0_0
pyodbc                    4.0.34          py310h6a678d5_0
pyopenssl                 23.0.0          py310h06a4308_0
pyparsing                 3.0.9           py310h06a4308_0
pyqt                      5.15.7          py310h6a678d5_1
pyqt5-sip                 12.11.0                  pypi_0    pypi
pyqtwebengine             5.15.7          py310h6a678d5_1
pyrsistent                0.18.0          py310h7f8727e_0
pysocks                   1.7.1           py310h06a4308_0
pytables                  3.7.0           py310hf19a122_1
pytest                    7.1.2           py310h06a4308_0
python                    3.10.9               h7a1cb2a_1
python-dateutil           2.8.2              pyhd3eb1b0_0
python-fastjsonschema     2.16.2          py310h06a4308_0
python-libarchive-c       2.9                pyhd3eb1b0_1
python-lsp-black          1.2.1           py310h06a4308_0
python-lsp-jsonrpc        1.0.0              pyhd3eb1b0_0
python-lsp-server         1.7.1           py310h06a4308_0
python-slugify            5.0.2              pyhd3eb1b0_0
python-snappy             0.6.1           py310h6a678d5_0
pytoolconfig              1.2.5           py310h06a4308_1
pytorch                   1.12.1          cpu_py310hb1f1ab4_1
pytz                      2022.7          py310h06a4308_0
pyviz_comms               2.0.2              pyhd3eb1b0_0
pywavelets                1.4.1           py310h5eee18b_0
pyxdg                     0.27               pyhd3eb1b0_0
pyyaml                    6.0             py310h5eee18b_1
pyzmq                     23.2.0          py310h6a678d5_0
qdarkstyle                3.0.2              pyhd3eb1b0_0
qstylizer                 0.2.2           py310h06a4308_0
qt-main                   5.15.2               h327a75a_7
qt-webengine              5.15.9               hd2b0992_4
qtawesome                 1.2.2           py310h06a4308_0
qtconsole                 5.4.0           py310h06a4308_0
qtpy                      2.2.0           py310h06a4308_0
qtwebkit                  5.212                h4eab89a_4
queuelib                  1.5.0           py310h06a4308_0
readline                  8.2                  h5eee18b_0
regex                     2022.7.9        py310h5eee18b_0
requests                  2.28.1          py310h06a4308_0
requests-file             1.5.1              pyhd3eb1b0_0
requests-toolbelt         0.9.1              pyhd3eb1b0_0
ripgrep                   13.0.0               hbdeaff8_0
rope                      1.7.0           py310h06a4308_0
rtree                     1.0.1           py310h06a4308_0
ruamel.yaml               0.17.21         py310h5eee18b_0
ruamel.yaml.clib          0.2.6           py310h5eee18b_1
ruamel_yaml               0.17.21         py310h5eee18b_0
scikit-image              0.19.3          py310h6a678d5_1
scikit-learn              1.2.1           py310h6a678d5_0
scikit-learn-intelex      2023.0.2        py310h06a4308_0
scipy                     1.10.0          py310hd5efca6_1
scrapy                    2.8.0           py310h06a4308_0
seaborn                   0.12.2          py310h06a4308_0
secretstorage             3.3.1           py310h06a4308_0
send2trash                1.8.0              pyhd3eb1b0_1
service_identity          18.1.0             pyhd3eb1b0_1
setuptools                65.6.3          py310h06a4308_0
sip                       6.6.2           py310h6a678d5_0
six                       1.16.0             pyhd3eb1b0_1
smart_open                5.2.1           py310h06a4308_0
snappy                    1.1.9                h295c915_0
sniffio                   1.2.0           py310h06a4308_1
snowballstemmer           2.2.0              pyhd3eb1b0_0
sortedcontainers          2.4.0              pyhd3eb1b0_0
soupsieve                 2.3.2.post1     py310h06a4308_0
sphinx                    5.0.2           py310h06a4308_0
sphinxcontrib-applehelp   1.0.2              pyhd3eb1b0_0
sphinxcontrib-devhelp     1.0.2              pyhd3eb1b0_0
sphinxcontrib-htmlhelp    2.0.0              pyhd3eb1b0_0
sphinxcontrib-jsmath      1.0.1              pyhd3eb1b0_0
sphinxcontrib-qthelp      1.0.3              pyhd3eb1b0_0
sphinxcontrib-serializinghtml 1.1.5              pyhd3eb1b0_0
spyder                    5.4.1           py310h06a4308_0
spyder-kernels            2.4.1           py310h06a4308_0
sqlalchemy                1.4.39          py310h5eee18b_0
sqlite                    3.40.1               h5082296_0
stack_data                0.2.0              pyhd3eb1b0_0
statsmodels               0.13.5          py310ha9d4c09_1
sympy                     1.11.1          py310h06a4308_0
tabulate                  0.8.10          py310h06a4308_0
tbb                       2021.7.0             hdb19cb5_0
tbb4py                    2021.7.0        py310hdb19cb5_0
tblib                     1.7.0              pyhd3eb1b0_0
tenacity                  8.0.1           py310h06a4308_1
terminado                 0.17.1          py310h06a4308_0
text-unidecode            1.3                pyhd3eb1b0_0
textdistance              4.2.1              pyhd3eb1b0_0
threadpoolctl             2.2.0              pyh0d69192_0
three-merge               0.1.1              pyhd3eb1b0_0
tifffile                  2021.7.2           pyhd3eb1b0_2
tinycss2                  1.2.1           py310h06a4308_0
tk                        8.6.12               h1ccaba5_0
tldextract                3.2.0              pyhd3eb1b0_0
tokenizers                0.11.4          py310h3dcd8bd_1
toml                      0.10.2             pyhd3eb1b0_0
tomli                     2.0.1           py310h06a4308_0
tomlkit                   0.11.1          py310h06a4308_0
toolz                     0.12.0          py310h06a4308_0
tornado                   6.1             py310h7f8727e_0
tqdm                      4.64.1          py310h06a4308_0
traitlets                 5.7.1           py310h06a4308_0
transformers              4.24.0          py310h06a4308_0
twisted                   22.2.0          py310h5eee18b_1
typing-extensions         4.4.0           py310h06a4308_0
typing_extensions         4.4.0           py310h06a4308_0
tzdata                    2022g                h04d1e81_0
ujson                     5.4.0           py310h6a678d5_0
unidecode                 1.2.0              pyhd3eb1b0_0
unixodbc                  2.3.11               h5eee18b_0
urllib3                   1.26.14         py310h06a4308_0
w3lib                     1.21.0             pyhd3eb1b0_0
watchdog                  2.1.6           py310h06a4308_0
wcwidth                   0.2.5              pyhd3eb1b0_0
webencodings              0.5.1           py310h06a4308_1
websocket-client          0.58.0          py310h06a4308_4
werkzeug                  2.2.2           py310h06a4308_0
whatthepatch              1.0.2           py310h06a4308_0
wheel                     0.38.4          py310h06a4308_0
widgetsnbextension        3.5.2           py310h06a4308_0
wrapt                     1.14.1          py310h5eee18b_0
wurlitzer                 3.0.2           py310h06a4308_0
xarray                    2022.11.0       py310h06a4308_0
xz                        5.2.10               h5eee18b_1
yaml                      0.2.5                h7b6447c_0
yapf                      0.31.0             pyhd3eb1b0_0
zeromq                    4.3.4                h2531618_0
zfp                       0.5.5                h295c915_6
zict                      2.1.0           py310h06a4308_0
zipp                      3.11.0          py310h06a4308_0
zlib                      1.2.13               h5eee18b_0
zope                      1.0             py310h06a4308_1
zope.interface            5.4.0           py310h7f8727e_0
zstandard                 0.19.0          py310h5eee18b_0
zstd                      1.5.2                ha4553b6_0
$

```
