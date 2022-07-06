#use cadCAD to generate a system model for the following system:
#a simulation of a simple spring-mass-damper system

import cadCAD.configuration as configuration
import cadCAD.cadcad as cadcad

configuration.set_configuration(
    {
        'system_name': 'AB', # name of the system
        'time_step': 0.1, # time step of the system
        'total_time': 10.0, # total time of the simulation
        'end_time_event': True, # end time event
        'end_time': 10.0, # end time of the simulation
        'stop_on_error': True, # stop simulation on error
        'debug_mode': False, # debug mode
        'random_seed': 0, # random seed
        'numerical_debug_mode': False, # numerical debug mode
        'numerical_debug_file': '', # numerical debug file
        'numerical_debug_update_time': 0.1, # numerical debug update time
        'numerical_debug_initial_state': False, # numerical debug initial state
        'numerical_debug_final_state': False, # numerical debug final state
        'numerical_debug_initial_state_file': '', # numerical debug initial state file
        'numerical_debug_final_state_file': '', # numerical debug final state file
        'numerical_debug_time_series': False, # numerical debug time series
        'numerical_debug_time_series_file': '', # numerical debug time series file
        'numerical_debug_time_series_update_time': 0.1, # numerical debug time series update time
        'numerical_debug_time_series_initial_state': False, # numerical debug time series initial state
        'numerical_debug_time_series_final_state': False,  # numerical debug time series final state

        'simulation_method': 'explicit', # simulation method
        'simulation_method_params': { # simulation method parameters
            'method': 'RK4', # method
            'tolerance': 1e-6, # tolerance
            'max_iterations': 100, # max iterations
            'max_order': 5, # max order
            'initial_step': 0.1, # initial step
            'min_step': 0.001, # min step
            'max_step': 1.0, # max step
            'adaptive': True, # adaptive
            'adaptive_params': { # adaptive parameters
                'tolerance': 1e-6, # tolerance
                'safety': 0.9, # safety
                'min_step': 0.001, # min step
                'max_step': 1.0, # max step
                'max_order': 5, # max order
                'order_reduction_factor': 0.9, # order reduction factor
                'order_increase_factor': 1.1, # order increase factor
                'max_order_increase': 5, # max order increase
                'max_order_decrease': 5, # max order decrease
                'max_order_increase_on_failure': 5, # max order increase on failure
                'max_order_decrease_on_failure': 5, # max order decrease on failure
                'max_order_increase_on_error': 5, # max order increase on error
                'max_order_decrease_on_error': 5, # max order decrease on error
                'max_order_increase_on_event': 5, # max order increase on event
                'max_order_decrease_on_event': 5, # max order decrease on event
                'max_order_increase_on_event_failure': 5, # max order increase on event failure
                'max_order_decrease_on_event_failure': 5, # max order decrease on event failure
                'max_order_increase_on_event_error': 5, # max order increase on event error
                'max_order_decrease_on_event_error': 5, # max order decrease on event error
                'max_order_increase_on_event_success': 5, # max order increase on event success
                'max_order_decrease_on_event_success': 5, # max order decrease on event success
                'max_order_increase_on_event_failure_error': 5, # max order increase on event failure error
                'max_order_decrease_on_event_failure_error': 5, # max order decrease on event failure error
                'max_order_increase_on_event_success_error': 5, # max order increase on event success error
                'max_order_decrease_on_event_success_error': 5, # max order decrease on event success error
                'max_order_increase_on_event_success_failure': 5, # max order increase on event success failure
                'max_order_decrease_on_event_success_failure': 5, # max order decrease on event success failure

def main():
    # create a new cadCAD object
    cadcad_object = cadcad.cadCAD()

    # create a new system model
    system_model_AB_exp = cadcad_object.new_system_model(
        name='AB_exp', # name of the system model
        parameters={ # parameters of the system model
            'm': 1.0, # mass of the spring
            'k': 1.0, # spring constant
            'c': 1.0, # damping constant
        },
        inputs={ # inputs of the system model
            'u': { # input of the system model
                'type': 'real', # type of the input
                'rate': 1.0, # rate of the input
                'value': 1.0, # value of the input
            },
        },
        outputs={ # outputs of the system model
            'y': { # output of the system model
                'type': 'real', # type of the output
                'rate': 1.0, # rate of the output
                'value': 0.0, # value of the output
            },  
        },              
        equations={ # equations of the system model
            'y': { # equation of the system model
                'type': 'real', # type of the equation
                'value': 'm*u + c*y/k', # value of the equation
            },  
        },
    )
    
