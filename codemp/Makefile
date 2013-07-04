PLATFORM=$(shell uname|tr A-Z a-z)

CC				= gcc
CXX				= g++
B				= Build
INST			= Install
BASE    		= Base
JAMPG    		= jampgamei386
CG    			= cgamei386
UI    			= uii386
OPENJKDED    	= openjkded.i386
LIB	    		= lib

ifeq ($(PLATFORM),darwin)
	DLL_EXT		= dylib
else
	DLL_EXT		= so
endif

GAME_NAME		= $(B)/$(INST)/$(BASE)/jampgamei386.$(DLL_EXT)
GAME_CFLAGS		= -m32 -Wall -Wno-comment -O3 -fPIC -I. -DQAGAME -D_JK2 -DNDEBUG -DFINAL_BUILD
GAME_LDFLAGS	= -m32 -shared -lm
GAME_OBJS		= $(B)/$(JAMPG)/game/ai_main.o \
				  $(B)/$(JAMPG)/game/ai_util.o \
				  $(B)/$(JAMPG)/game/ai_wpnav.o \
				  $(B)/$(JAMPG)/game/AnimalNPC.o \
				  $(B)/$(JAMPG)/game/bg_g2_utils.o \
				  $(B)/$(JAMPG)/game/bg_misc.o \
				  $(B)/$(JAMPG)/game/bg_panimate.o \
				  $(B)/$(JAMPG)/game/bg_pmove.o \
				  $(B)/$(JAMPG)/game/bg_saber.o \
				  $(B)/$(JAMPG)/game/bg_saberLoad.o \
				  $(B)/$(JAMPG)/game/bg_saga.o \
				  $(B)/$(JAMPG)/game/bg_slidemove.o \
				  $(B)/$(JAMPG)/game/bg_vehicleLoad.o \
				  $(B)/$(JAMPG)/game/bg_weapons.o \
				  $(B)/$(JAMPG)/game/FighterNPC.o \
				  $(B)/$(JAMPG)/game/g_active.o \
				  $(B)/$(JAMPG)/game/g_bot.o \
				  $(B)/$(JAMPG)/game/g_client.o \
				  $(B)/$(JAMPG)/game/g_cmds.o \
				  $(B)/$(JAMPG)/game/g_combat.o \
				  $(B)/$(JAMPG)/game/g_cvar.o \
				  $(B)/$(JAMPG)/game/g_exphysics.o \
				  $(B)/$(JAMPG)/game/g_ICARUScb.o \
				  $(B)/$(JAMPG)/game/g_items.o \
				  $(B)/$(JAMPG)/game/g_log.o \
				  $(B)/$(JAMPG)/game/g_main.o \
				  $(B)/$(JAMPG)/game/g_mem.o \
				  $(B)/$(JAMPG)/game/g_misc.o \
				  $(B)/$(JAMPG)/game/g_missile.o \
				  $(B)/$(JAMPG)/game/g_mover.o \
				  $(B)/$(JAMPG)/game/g_nav.o \
				  $(B)/$(JAMPG)/game/g_navnew.o \
				  $(B)/$(JAMPG)/game/g_object.o \
				  $(B)/$(JAMPG)/game/g_saga.o \
				  $(B)/$(JAMPG)/game/g_session.o \
				  $(B)/$(JAMPG)/game/g_spawn.o \
				  $(B)/$(JAMPG)/game/g_strap.o \
				  $(B)/$(JAMPG)/game/g_svcmds.o \
				  $(B)/$(JAMPG)/game/g_syscalls.o \
				  $(B)/$(JAMPG)/game/g_target.o \
				  $(B)/$(JAMPG)/game/g_team.o \
				  $(B)/$(JAMPG)/game/g_timer.o \
				  $(B)/$(JAMPG)/game/g_trigger.o \
				  $(B)/$(JAMPG)/game/g_turret_G2.o \
				  $(B)/$(JAMPG)/game/g_turret.o \
				  $(B)/$(JAMPG)/game/g_utils.o \
				  $(B)/$(JAMPG)/game/g_vehicles.o \
				  $(B)/$(JAMPG)/game/g_vehicleTurret.o \
				  $(B)/$(JAMPG)/game/g_weapon.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Atst.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Default.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Droid.o \
				  $(B)/$(JAMPG)/game/NPC_AI_GalakMech.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Grenadier.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Howler.o \
				  $(B)/$(JAMPG)/game/NPC_AI_ImperialProbe.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Interrogator.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Jedi.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Mark1.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Mark2.o \
				  $(B)/$(JAMPG)/game/NPC_AI_MineMonster.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Rancor.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Remote.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Seeker.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Sentry.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Sniper.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Stormtrooper.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Utils.o \
				  $(B)/$(JAMPG)/game/NPC_AI_Wampa.o \
				  $(B)/$(JAMPG)/game/NPC_behavior.o \
				  $(B)/$(JAMPG)/game/NPC_combat.o \
				  $(B)/$(JAMPG)/game/NPC_goal.o \
				  $(B)/$(JAMPG)/game/NPC_misc.o \
				  $(B)/$(JAMPG)/game/NPC_move.o \
				  $(B)/$(JAMPG)/game/NPC_reactions.o \
				  $(B)/$(JAMPG)/game/NPC_senses.o \
				  $(B)/$(JAMPG)/game/NPC_sounds.o \
				  $(B)/$(JAMPG)/game/NPC_spawn.o \
				  $(B)/$(JAMPG)/game/NPC_stats.o \
				  $(B)/$(JAMPG)/game/NPC_utils.o \
				  $(B)/$(JAMPG)/game/NPC.o \
				  $(B)/$(JAMPG)/game/SpeederNPC.o \
				  $(B)/$(JAMPG)/game/tri_coll_test.o \
				  $(B)/$(JAMPG)/game/w_force.o \
				  $(B)/$(JAMPG)/game/w_saber.o \
				  $(B)/$(JAMPG)/game/WalkerNPC.o \
				  $(B)/$(JAMPG)/qcommon/q_math.o \
				  $(B)/$(JAMPG)/qcommon/q_shared.o

CGAME_NAME		= $(B)/$(INST)/$(BASE)/cgamei386.$(DLL_EXT)
CGAME_CFLAGS	= -m32 -Wall -Wno-comment -O3 -fPIC -I. -DCGAME -D_JK2 -DNDEBUG -DFINAL_BUILD
CGAME_LDFLAGS	= -m32 -shared -lm
CGAME_OBJS		= $(B)/$(CG)/cgame/cg_consolecmds.o \
				  $(B)/$(CG)/cgame/cg_draw.o \
				  $(B)/$(CG)/cgame/cg_drawtools.o \
				  $(B)/$(CG)/cgame/cg_effects.o \
				  $(B)/$(CG)/cgame/cg_ents.o \
				  $(B)/$(CG)/cgame/cg_event.o \
				  $(B)/$(CG)/cgame/cg_info.o \
				  $(B)/$(CG)/cgame/cg_light.o \
				  $(B)/$(CG)/cgame/cg_localents.o \
				  $(B)/$(CG)/cgame/cg_main.o \
				  $(B)/$(CG)/cgame/cg_marks.o \
				  $(B)/$(CG)/cgame/cg_newDraw.o \
				  $(B)/$(CG)/cgame/cg_players.o \
				  $(B)/$(CG)/cgame/cg_playerstate.o \
				  $(B)/$(CG)/cgame/cg_predict.o \
				  $(B)/$(CG)/cgame/cg_saga.o \
				  $(B)/$(CG)/cgame/cg_scoreboard.o \
				  $(B)/$(CG)/cgame/cg_servercmds.o \
				  $(B)/$(CG)/cgame/cg_snapshot.o \
				  $(B)/$(CG)/cgame/cg_spawn.o \
				  $(B)/$(CG)/cgame/cg_strap.o \
				  $(B)/$(CG)/cgame/cg_syscalls.o \
				  $(B)/$(CG)/cgame/cg_turret.o \
				  $(B)/$(CG)/cgame/cg_view.o \
				  $(B)/$(CG)/cgame/cg_weaponinit.o \
				  $(B)/$(CG)/cgame/cg_weapons.o \
				  $(B)/$(CG)/cgame/fx_blaster.o \
				  $(B)/$(CG)/cgame/fx_bowcaster.o \
				  $(B)/$(CG)/cgame/fx_bryarpistol.o \
				  $(B)/$(CG)/cgame/fx_demp2.o \
				  $(B)/$(CG)/cgame/fx_disruptor.o \
				  $(B)/$(CG)/cgame/fx_flechette.o \
				  $(B)/$(CG)/cgame/fx_force.o \
				  $(B)/$(CG)/cgame/fx_heavyrepeater.o \
				  $(B)/$(CG)/cgame/fx_rocketlauncher.o \
				  $(B)/$(CG)/game/AnimalNPC.o \
				  $(B)/$(CG)/game/bg_g2_utils.o \
				  $(B)/$(CG)/game/bg_misc.o \
				  $(B)/$(CG)/game/bg_panimate.o \
				  $(B)/$(CG)/game/bg_pmove.o \
				  $(B)/$(CG)/game/bg_saber.o \
				  $(B)/$(CG)/game/bg_saberLoad.o \
				  $(B)/$(CG)/game/bg_saga.o \
				  $(B)/$(CG)/game/bg_slidemove.o \
				  $(B)/$(CG)/game/bg_vehicleLoad.o \
				  $(B)/$(CG)/game/bg_weapons.o \
				  $(B)/$(CG)/game/FighterNPC.o \
				  $(B)/$(CG)/game/SpeederNPC.o \
				  $(B)/$(CG)/game/WalkerNPC.o \
				  $(B)/$(CG)/qcommon/q_math.o \
				  $(B)/$(CG)/qcommon/q_shared.o \
				  $(B)/$(CG)/ui/ui_shared.o

UI_NAME			= $(B)/$(INST)/$(BASE)/uii386.$(DLL_EXT)
UI_CFLAGS		= -m32 -Wall -Wno-comment -O3 -fPIC -I. -DUI_EXPORTS -D_JK2 -DNDEBUG -DFINAL_BUILD
UI_LDFLAGS		= -m32 -shared -lm
UI_OBJS			= $(B)/$(UI)/ui/ui_atoms.o \
				  $(B)/$(UI)/game/bg_misc.o \
				  $(B)/$(UI)/game/bg_saga.o \
				  $(B)/$(UI)/game/bg_vehicleLoad.o \
				  $(B)/$(UI)/game/bg_weapons.o \
				  $(B)/$(UI)/qcommon/q_math.o \
				  $(B)/$(UI)/qcommon/q_shared.o \
				  $(B)/$(UI)/ui/ui_force.o \
				  $(B)/$(UI)/ui/ui_gameinfo.o \
				  $(B)/$(UI)/ui/ui_main.o \
				  $(B)/$(UI)/ui/ui_saber.o \
				  $(B)/$(UI)/ui/ui_shared.o \
				  $(B)/$(UI)/ui/ui_syscalls.o

OPENJKDED_NAME		= $(B)/$(INST)/openjkded.i386
OPENJKDED_CFLAGS	= -m32 -Wall -Wno-comment -O3 -I. -I../lib -D_JK2 -DDEDICATED -DNDEBUG -DFINAL_BUILD
OPENJKDED_LDFLAGS	= -m32 -ldl -lz
OPENJKDED_OBJS		= $(B)/$(OPENJKDED)/botlib/be_aas_bspq3.o \
					  $(B)/$(OPENJKDED)/botlib/be_aas_cluster.o \
					  $(B)/$(OPENJKDED)/botlib/be_aas_debug.o \
					  $(B)/$(OPENJKDED)/botlib/be_aas_entity.o \
					  $(B)/$(OPENJKDED)/botlib/be_aas_file.o \
				 	  $(B)/$(OPENJKDED)/botlib/be_aas_main.o \
					  $(B)/$(OPENJKDED)/botlib/be_aas_move.o \
					  $(B)/$(OPENJKDED)/botlib/be_aas_optimize.o \
				      $(B)/$(OPENJKDED)/botlib/be_aas_reach.o \
					  $(B)/$(OPENJKDED)/botlib/be_aas_route.o \
					  $(B)/$(OPENJKDED)/botlib/be_aas_routealt.o \
					  $(B)/$(OPENJKDED)/botlib/be_aas_sample.o \
					  $(B)/$(OPENJKDED)/botlib/be_ai_char.o \
					  $(B)/$(OPENJKDED)/botlib/be_ai_chat.o \
					  $(B)/$(OPENJKDED)/botlib/be_ai_gen.o \
					  $(B)/$(OPENJKDED)/botlib/be_ai_goal.o \
					  $(B)/$(OPENJKDED)/botlib/be_ai_move.o \
					  $(B)/$(OPENJKDED)/botlib/be_ai_weap.o \
					  $(B)/$(OPENJKDED)/botlib/be_ai_weight.o \
					  $(B)/$(OPENJKDED)/botlib/be_ea.o \
					  $(B)/$(OPENJKDED)/botlib/be_interface.o \
					  $(B)/$(OPENJKDED)/botlib/l_crc.o \
					  $(B)/$(OPENJKDED)/botlib/l_libvar.o \
					  $(B)/$(OPENJKDED)/botlib/l_log.o \
					  $(B)/$(OPENJKDED)/botlib/l_memory.o \
					  $(B)/$(OPENJKDED)/botlib/l_precomp.o \
					  $(B)/$(OPENJKDED)/botlib/l_script.o \
					  $(B)/$(OPENJKDED)/botlib/l_struct.o \
					  $(B)/$(OPENJKDED)/icarus/BlockStream.o \
					  $(B)/$(OPENJKDED)/icarus/GameInterface.o \
					  $(B)/$(OPENJKDED)/icarus/Instance.o \
					  $(B)/$(OPENJKDED)/icarus/Interface.o \
					  $(B)/$(OPENJKDED)/icarus/Memory.o \
					  $(B)/$(OPENJKDED)/icarus/Q3_Interface.o \
					  $(B)/$(OPENJKDED)/icarus/Q3_Registers.o \
					  $(B)/$(OPENJKDED)/icarus/Sequence.o \
					  $(B)/$(OPENJKDED)/icarus/Sequencer.o \
					  $(B)/$(OPENJKDED)/icarus/TaskManager.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/png.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngerror.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngget.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngmem.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngpread.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngread.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngrio.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngrtran.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngrutil.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngset.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngtrans.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngwio.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngwrite.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngwtran.o \
					  $(B)/$(OPENJKDED)/$(LIB)/libpng/pngwutil.o \
					  $(B)/$(OPENJKDED)/null/null_client.o \
					  $(B)/$(OPENJKDED)/null/null_input.o \
					  $(B)/$(OPENJKDED)/null/null_renderer.o \
					  $(B)/$(OPENJKDED)/null/null_snddma.o \
					  $(B)/$(OPENJKDED)/qcommon/cm_draw.o \
					  $(B)/$(OPENJKDED)/qcommon/cm_load.o \
					  $(B)/$(OPENJKDED)/qcommon/cm_patch.o \
					  $(B)/$(OPENJKDED)/qcommon/cm_polylib.o \
					  $(B)/$(OPENJKDED)/qcommon/cm_randomterrain.o \
					  $(B)/$(OPENJKDED)/qcommon/cm_shader.o \
					  $(B)/$(OPENJKDED)/qcommon/cm_terrain.o \
					  $(B)/$(OPENJKDED)/qcommon/cm_test.o \
					  $(B)/$(OPENJKDED)/qcommon/cm_trace.o \
					  $(B)/$(OPENJKDED)/qcommon/cmd_common.o \
					  $(B)/$(OPENJKDED)/qcommon/cmd_pc.o \
					  $(B)/$(OPENJKDED)/qcommon/common.o \
					  $(B)/$(OPENJKDED)/qcommon/cvar.o \
					  $(B)/$(OPENJKDED)/qcommon/files_common.o \
					  $(B)/$(OPENJKDED)/qcommon/files_pc.o \
					  $(B)/$(OPENJKDED)/qcommon/GenericParser2.o \
					  $(B)/$(OPENJKDED)/qcommon/huffman.o \
					  $(B)/$(OPENJKDED)/qcommon/matcomp.o \
					  $(B)/$(OPENJKDED)/qcommon/md4.o \
					  $(B)/$(OPENJKDED)/qcommon/msg.o \
					  $(B)/$(OPENJKDED)/qcommon/net_chan.o \
					  $(B)/$(OPENJKDED)/qcommon/q_math.o \
					  $(B)/$(OPENJKDED)/qcommon/q_shared.o \
					  $(B)/$(OPENJKDED)/qcommon/RoffSystem.o \
					  $(B)/$(OPENJKDED)/qcommon/stringed_ingame.o \
					  $(B)/$(OPENJKDED)/qcommon/stringed_interface.o \
					  $(B)/$(OPENJKDED)/qcommon/unzip.o \
					  $(B)/$(OPENJKDED)/qcommon/vm_interpreted.o \
					  $(B)/$(OPENJKDED)/qcommon/vm.o \
					  $(B)/$(OPENJKDED)/qcommon/z_memman_pc.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/G2_API.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/G2_bolts.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/G2_bones.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/G2_misc.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/G2_surfaces.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/tr_backend.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/tr_ghoul2.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/tr_image.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/tr_init.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/tr_main.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/tr_mesh.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/tr_model.o \
					  $(B)/$(OPENJKDED)/rd-dedicated/tr_shader.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Area.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Instance_BSP.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Instance_Group.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Instance_Random.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Instance_Void.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Instance.o \
					  $(B)/$(OPENJKDED)/RMG/RM_InstanceFile.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Manager.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Mission.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Objective.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Path.o \
					  $(B)/$(OPENJKDED)/RMG/RM_Terrain.o \
					  $(B)/$(OPENJKDED)/server/NPCNav/gameCallbacks.o \
					  $(B)/$(OPENJKDED)/server/NPCNav/navigator.o \
					  $(B)/$(OPENJKDED)/server/sv_bot.o \
					  $(B)/$(OPENJKDED)/server/sv_ccmds.o \
					  $(B)/$(OPENJKDED)/server/sv_client.o \
					  $(B)/$(OPENJKDED)/server/sv_game.o \
					  $(B)/$(OPENJKDED)/server/sv_init.o \
					  $(B)/$(OPENJKDED)/server/sv_main.o \
					  $(B)/$(OPENJKDED)/server/sv_net_chan.o \
					  $(B)/$(OPENJKDED)/server/sv_snapshot.o \
					  $(B)/$(OPENJKDED)/server/sv_world.o \
					  $(B)/$(OPENJKDED)/sys/snapvector.o \
					  $(B)/$(OPENJKDED)/sys/sys_main.o \
					  $(B)/$(OPENJKDED)/sys/sys_net.o \
					  $(B)/$(OPENJKDED)/sys/sys_unix.o \
					  $(B)/$(OPENJKDED)/sys/vm_x86.o \
					  $(B)/$(OPENJKDED)/$(LIB)/zlib/ioapi.o

ifeq ($(PLATFORM),darwin)
	OPENJKDED_CFLAGS += -DMACOS_X
	CGAME_CFLAGS += -DMACOS_X
	GAME_CFLAGS += -DMACOS_X
	UI_CFLAGS += -DMACOS_X
else
	GAME_CFLAGS += -D__linux__
	CGAME_CFLAGS += -D__linux__
	UI_CFLAGS += -D__linux__
	OPENJKDED_CFLAGS += -D__linux__
endif

all: makedirs game cgame ui openjkded

makedirs:
	@if [ ! -d $(B) ];then mkdir $(B);fi
	@if [ ! -d $(B)/$(INST) ];then mkdir $(B)/$(INST);fi
	@if [ ! -d $(B)/$(INST)/$(BASE) ];then mkdir $(B)/$(INST)/$(BASE);fi
	@if [ ! -d $(B)/$(JAMPG) ];then mkdir $(B)/$(JAMPG);fi
	@if [ ! -d $(B)/$(JAMPG)/game ];then mkdir $(B)/$(JAMPG)/game;fi
	@if [ ! -d $(B)/$(JAMPG)/qcommon ];then mkdir $(B)/$(JAMPG)/qcommon;fi
	@if [ ! -d $(B)/$(CG) ];then mkdir $(B)/$(CG);fi
	@if [ ! -d $(B)/$(CG)/cgame ];then mkdir $(B)/$(CG)/cgame;fi
	@if [ ! -d $(B)/$(CG)/game ];then mkdir $(B)/$(CG)/game;fi
	@if [ ! -d $(B)/$(CG)/qcommon ];then mkdir $(B)/$(CG)/qcommon;fi
	@if [ ! -d $(B)/$(CG)/ui ];then mkdir $(B)/$(CG)/ui;fi
	@if [ ! -d $(B)/$(UI) ];then mkdir $(B)/$(UI);fi
	@if [ ! -d $(B)/$(UI)/game ];then mkdir $(B)/$(UI)/game;fi
	@if [ ! -d $(B)/$(UI)/qcommon ];then mkdir $(B)/$(UI)/qcommon;fi
	@if [ ! -d $(B)/$(UI)/ui ];then mkdir $(B)/$(UI)/ui;fi
	@if [ ! -d $(B)/$(OPENJKDED) ];then mkdir $(B)/$(OPENJKDED);fi
	@if [ ! -d $(B)/$(OPENJKDED)/botlib ];then mkdir $(B)/$(OPENJKDED)/botlib;fi
	@if [ ! -d $(B)/$(OPENJKDED)/icarus ];then mkdir $(B)/$(OPENJKDED)/icarus;fi
	@if [ ! -d $(B)/$(OPENJKDED)/$(LIB) ];then mkdir $(B)/$(OPENJKDED)/$(LIB);fi
	@if [ ! -d $(B)/$(OPENJKDED)/$(LIB)/libpng ];then mkdir $(B)/$(OPENJKDED)/$(LIB)/libpng;fi
	@if [ ! -d $(B)/$(OPENJKDED)/null ];then mkdir $(B)/$(OPENJKDED)/null;fi
	@if [ ! -d $(B)/$(OPENJKDED)/qcommon ];then mkdir $(B)/$(OPENJKDED)/qcommon;fi
	@if [ ! -d $(B)/$(OPENJKDED)/rd-dedicated ];then mkdir $(B)/$(OPENJKDED)/rd-dedicated;fi
	@if [ ! -d $(B)/$(OPENJKDED)/RMG ];then mkdir $(B)/$(OPENJKDED)/RMG;fi
	@if [ ! -d $(B)/$(OPENJKDED)/server ];then mkdir $(B)/$(OPENJKDED)/server;fi
	@if [ ! -d $(B)/$(OPENJKDED)/server/NPCNav ];then mkdir $(B)/$(OPENJKDED)/server/NPCNav;fi
	@if [ ! -d $(B)/$(OPENJKDED)/sys ];then mkdir $(B)/$(OPENJKDED)/sys;fi
	@if [ ! -d $(B)/$(OPENJKDED)/$(LIB)/zlib ];then mkdir $(B)/$(OPENJKDED)/$(LIB)/zlib;fi

#
# GAME RULES
#

game: $(GAME_NAME)

$(GAME_NAME): $(GAME_OBJS)
	$(CC) -o $(GAME_NAME) $(GAME_OBJS) $(GAME_LDFLAGS)

$(B)/$(JAMPG)/game/%.o: game/%.c
	$(CC) $(GAME_CFLAGS) -c $< -o $@

$(B)/$(JAMPG)/qcommon/q_%.o: qcommon/q_%.c
	$(CC) $(GAME_CFLAGS) -D_M_IX86 -Did386 -c $< -o $@

#
# CGAME RULES
#

cgame: $(CGAME_NAME)

$(CGAME_NAME): $(CGAME_OBJS)
	$(CC) -o $(CGAME_NAME) $(CGAME_OBJS) $(CGAME_LDFLAGS)

$(B)/$(CG)/cgame/%.o: cgame/%.c
	$(CC) $(CGAME_CFLAGS) -c $< -o $@

$(B)/$(CG)/game/%NPC.o: game/%NPC.c
	$(CC) $(CGAME_CFLAGS) -c $< -o $@

$(B)/$(CG)/game/bg_%.o: game/bg_%.c
	$(CC) $(CGAME_CFLAGS) -c $< -o $@

$(B)/$(CG)/qcommon/q_%.o: qcommon/q_%.c
	$(CC) $(CGAME_CFLAGS) -D_M_IX86 -Did386 -c $< -o $@

$(B)/$(CG)/ui/ui_%.o: ui/ui_%.c
	$(CC) $(CGAME_CFLAGS) -c $< -o $@

#
# UI RULES
#

ui: $(UI_NAME)

$(UI_NAME): $(UI_OBJS)
	$(CC) -o $(UI_NAME) $(UI_OBJS) $(UI_LDFLAGS)

$(B)/$(UI)/game/bg_%.o: game/bg_%.c
	$(CC) $(UI_CFLAGS) -c $< -o $@	

$(B)/$(UI)/qcommon/q_%.o: qcommon/q_%.c
	$(CC) $(UI_CFLAGS) -D_M_IX86 -Did386 -c $< -o $@

$(B)/$(UI)/ui/%.o: ui/%.c
	$(CC) $(UI_CFLAGS) -c $< -o $@

#
# OPENJKDED RULES
#

openjkded: $(OPENJKDED_NAME)

$(OPENJKDED_NAME): $(OPENJKDED_OBJS)
	$(CXX) -o $(OPENJKDED_NAME) $(OPENJKDED_OBJS) $(OPENJKDED_LDFLAGS)

$(B)/$(OPENJKDED)/botlib/%.o: botlib/%.cpp
	$(CXX) $(OPENJKDED_CFLAGS)  -DBOTLIB -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@

$(B)/$(OPENJKDED)/icarus/%.o: icarus/%.cpp
	$(CXX) $(OPENJKDED_CFLAGS)  -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@

$(B)/$(OPENJKDED)/$(LIB)/libpng/%.o: ../$(LIB)/libpng/%.c
	$(CC) $(OPENJKDED_CFLAGS) -c $< -o $@

$(B)/$(OPENJKDED)/null/%.o: null/%.cpp
	$(CXX) $(OPENJKDED_CFLAGS)  -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@

$(B)/$(OPENJKDED)/qcommon/%.o: qcommon/%.cpp
	$(CXX) $(OPENJKDED_CFLAGS) -D_M_IX86 -Did386 -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@

$(B)/$(OPENJKDED)/rd-dedicated/%.o: rd-dedicated/%.cpp
	$(CXX) $(OPENJKDED_CFLAGS) -D_M_IX86 -Did386 -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@

$(B)/$(OPENJKDED)/RMG/%.o: RMG/%.cpp
	$(CXX) $(OPENJKDED_CFLAGS)  -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@

$(B)/$(OPENJKDED)/server/%.o: server/%.cpp
	$(CXX) $(OPENJKDED_CFLAGS)  -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@

$(B)/$(OPENJKDED)/server/NPCNav/%.o: server/NPCNav/%.cpp
	$(CXX) $(OPENJKDED_CFLAGS)  -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@

$(B)/$(OPENJKDED)/sys/%.o: sys/%.cpp
	$(CXX) $(OPENJKDED_CFLAGS)  -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@
	
$(B)/$(OPENJKDED)/sys/snapvector.o: sys/snapvector.cpp
	$(CXX) $(OPENJKDED_CFLAGS)  -Wno-invalid-offsetof -Wno-write-strings -c $< -o $@

$(B)/$(OPENJKDED)/$(LIB)/zlib/ioapi.o: ../$(LIB)/zlib/ioapi.c
	$(CC) $(OPENJKDED_CFLAGS) -c $< -o $@

clean:
	rm -rf $(B)

clean_game:
	$(RM) $(GAME_OBJS) \
	$(GAME_NAME)

clean_cgame:
	$(RM) $(CGAME_OBJS) \
	$(CGAME_NAME)

clean_ui:
	$(RM) $(UI_OBJS) \
	$(UI_NAME)

clean_openjkded:
	$(RM) $(OPENJKDED_OBJS) \
	$(OPENJKDED_NAME)
