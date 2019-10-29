Authors develop XAI-PLAN framework to help users explore alternative plans by 
suggesting different actions in the plan. The planning system is then used not only to generate the initial plan, 
but also to explore the alternative plans resulting from the user suggestions. 

Old planners for robotics are automatic and can not be intervented.

But here they introduce XAI-PLAN that allows us to intervent the action generation process (plan-making process). 
When we suggest another decision, the framwork will give response back about our intervention. For example,
it will show that by doing this option, we can not achieve this or that goal of the plan.

The framework is implemented using the ROSPlan framework, which provides an interface to A
I planning systems and a method for storing and modifying PDDL models in the Robot Operating System (ROS). 
The knowledge base, problem interface, and planner interface are supplied by ROSPlan, which are used to store a 
PDDL model and provide an interface to the AI planner. The interface was designed following a user-centered approach; 
each component either supports a user initiated action or caters for a possible user need, such as performance comparison 
or plan generation tracking.

**In which PDDL- Planning Domain Definition Language** is a langue for planning in robotics.
