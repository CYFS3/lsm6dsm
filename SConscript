from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()

src += Glob('driver/*.c')
if GetDepend('PKG_LSM6DSM_USING_SENSOR_V1'):
    src += Glob('lsm6dsm_sensor_v1.c')
# add lsm6dsm include path.
path  = [cwd, cwd + '/driver']

# add src and include to group.
group = DefineGroup('lsm6dsm', src, depend = ['PKG_USING_LSM6DSM'], CPPPATH = path)

Return('group')
