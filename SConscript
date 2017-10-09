from building import *

# get current dir path
cwd = GetCurrentDir()

# init src and inc vars
src = []
inc = []

# add clib list common include
inc = inc + [cwd + '/inc']

# add clib list basic code
src = src + ['./src/list.c']
src = src + ['./src/list_node.c']

# add clib list iterator code
if GetDepend('PKG_USING_CLIST_ITERATOR'):
	src = src + ['./src/list_iterator.c']

# add group to IDE project
group = DefineGroup('clist', src, depend = ['PKG_USING_CLIST'], CPPPATH = inc)

Return('group')
